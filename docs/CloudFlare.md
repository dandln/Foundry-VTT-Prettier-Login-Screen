# CloudFlare Installation 

You can install this with CloudFlare via a service worker to avoid editing foundry files and persist through updates. 
To do so, follow the steps below: 

## Open CloudFlare

1. Open and log into cloudflare. 
2. Click Workers after selecting your domain

![image](https://user-images.githubusercontent.com/12646562/123735030-4bc4b580-d853-11eb-9d76-a4efa47804f0.png)

## Add a new worker

1. Click Manage Workers
2. Create a new worker 
3. Paste the following script in

```js
addEventListener("fetch", (event) => {
  event.respondWith(
    handleRequest(event.request).catch(
      (err) => new Response(err.stack, { status: 500 })
    )
  );
});

class ElementHandler {
  element(element) {
    element.append(`<link
      rel="stylesheet" 
      type="text/css" 
      data-id="foundry-login"
      href="https://cdn.jsdelivr.net/gh/TheEpicSnowWolf/Foundry-VTT-Prettier-Login-Screen@main/foundry_login.css"  
    >`, {html: true});
    console.log("injected");
  }
}

async function handleRequest(req) {
  const res = await fetch(req)
  console.log(req)
  if (res.url.includes('YOUR.DOMAIN.NAME/join')) {
    return new HTMLRewriter().on("head", new ElementHandler()).transform(res)
  }  
  
  return fetch(req);
}
```

4. Change `YOUr.DOMAIN.NAME` to the one you are using with cloudflare to point to your foundry instance.
5. Save and deploy the worker.

## Complete configuration

1. On the worker configuration page (if your on the code screen, click the name of the worker in the upper left hand)
2. Disable the `workers.dev` domain for the worker. 
3. Next navigate back to your domain and click Workers again.
4. Click Add Route
5. add `YOUR.DOMAIN.NAME/join` as the route.
6. Select your worker for the route
7. Save


## Navigate to your Foundry domain

![image](https://user-images.githubusercontent.com/12646562/123735378-f341e800-d853-11eb-84e5-7e13102113fd.png)
