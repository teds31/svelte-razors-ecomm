<script>
  // router
  import { Router, Link, Route } from "svelte-routing";
  // pages
  import About from "./pages/About.svelte";
  import Checkout from "./pages/Checkout.svelte";
  import Home from "./pages/Home.svelte";
  import Login from "./pages/Login.svelte";
  import Products from "./pages/Products.svelte";
  import ProductTemplate from "./pages/ProductTemplate.svelte";
  // variables
  // export let id;
</script>

<Router>
  <nav class="navbar">
    <Link to="/">Home</Link>
    <Link to="/about">About</Link>
    <Link to="/products">Products</Link>
  </nav>
  <Route path="/" component={Home} />
  <Route path="/about" component={About} />
  <Route path="/login" component={Login} />
  <Route path="/products" component={Products} />
  <Route path="/products/:id" component={ProductTemplate} />
  <Route path="/checkout" component={Checkout} />
</Router>
