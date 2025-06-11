<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "A.J. Wong",
      position: "COO",
      company: "Bowlhaus",
      quote:
        "FUSICON cut our assembly time in half—and we haven’t had to hire in months.",
      image: "/generated/image-a-professional-asian-male-restaurant-coo.webp"
    },
    {
      name: "Lucia Navarro",
      position: "General Manager",
      company: "Dashi & Go",
      quote:
        "MOSAIC gave us real-time recipe costing and shift planning on one screen. It’s like magic for ops.",
      image: "/generated/image-a-confident-hispanic-female-restaurant-g.webp"
    },
    {
      name: "Omar Sayeed",
      position: "Chief Digital Officer",
      company: "Lana's Wraps",
      quote:
        "With KAIKAKU Intelligence, we launched personalized meals based on customers’ nutrition goals and saw a 21% increase in repeat orders.",
      image: "/generated/image-an-energetic-middle-eastern-male-restaur.webp"
    }
  ]}
/>

<CallToAction
  title="Ready for a restaurant that runs itself?"
  subtitle="See how KAIKAKU can transform your operation."
  description="Book a demo to experience robotics, AI, and intelligent software working together. Lower labor costs, faster service, and happier guests—finally, a restaurant system that keeps you in control."
  imageSrc="/generated/image-a-cheerful-restaurant-owner-standing-in-.webp"
  callsToAction={[
    { href: '/demo', label: 'Book a demo', variant: 'primary' },
    { href: '/contact', label: 'Talk to sales', variant: 'secondary' }
  ]}
/>

