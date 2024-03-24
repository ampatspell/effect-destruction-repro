## `$effect` destroy reproduction

```
$ npm run dev
```

* Open http://localhost:5173/
* Open developer tools → console
* Click on "/dev/thing" link
* Click on "back to index" (or browser's back button)

`/routes/dev/thing/+page.svelte` has `$effect`:

``` ts
$effect(() => {
  console.log('create');
  return () => {
    console.log('destroy');
  }
});
```

`$effect`'s destroy is not called if there is `/routes/dev/+layout.ts` (even if it's empty)

Sometimes also `<a href="/">` and `goto('/')` navigation stops working w/o any errors thrown.
