<script lang="ts">
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import { animate, stagger } from "motion";
	import { onMount } from "svelte";

	// Types
	export type Value = {
		title: string;
		description: string;
	};

	// Props
	const { values = [] }: { values: Value[] } = $props();

	let cards: HTMLElement[] = $state([]);

	onMount(() => {
		if (!cards.length) return;
		if (window.self !== window.top) return;

		animate(
			cards,
			{
				y: ["1.5rem", 0],
				filter: ["blur(2px)", "blur(0px)"],
				opacity: [0, 1]
			},
			{
				duration: 0.3,
				ease: "easeOut",
				delay: stagger(0.1, {
					ease: "easeInOut"
				})
			}
		);
	});
</script>

<section class="bg-white dark:bg-gray-950">
	<div
		class="section-py section-px container mx-auto grid gap-8 [--gap:--spacing(8)] [--radius:var(--radius-2xl)]"
	>
		<SectionHeader title="We're building the next generation of restaurant technology" subtitle="A culture for ambitious builders, engineers, and innovators" />
<div class="flex flex-col gap-8">
  <div class="text-body">
    <p>We’re an engineering-first company solving real-world problems with robotics and AI—from the rate of orders per hour to margins per shift. Our mission is clear: help QSRs scale without scaling complexity.</p>
  </div>
  <div class="grid gap-(--gap)" style:grid-template-columns="repeat(auto-fit, minmax(280px, 1fr))">
    <div class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
      <div class="text-caption z-10">
        <div>
          <div class="text-headline mb-[1em]">Engineering for hands-on impact</div>
          <div class="text-body text-gray-500 dark:text-gray-400">At KAIKAKU, you won't be tweaking legacy code from the sidelines. You’ll be in the code, on the assembly line, and inside test kitchens building systems that directly impact modern restaurants. From food-safe robotics to real-time operations software to personalized customer experiences—there’s no layer we don’t touch.</div>
        </div>
      </div>
    </div>
    <div class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
      <div class="text-caption z-10">
        <div>
          <div class="text-headline mb-[1em]">Ambition meets ownership</div>
          <div class="text-body text-gray-500 dark:text-gray-400">We're a young company backed by world-class investors, moving fast with a vertically integrated stack. That means higher leverage for engineers, faster decisions, and the chance to help write our playbook—not just follow one.</div>
        </div>
      </div>
    </div>
    <div class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
      <div class="text-caption z-10">
        <div>
          <div class="text-headline mb-[1em]">A place where builders belong</div>
          <div class="text-body text-gray-500 dark:text-gray-400">We’re looking for ambitious engineers, robotics and AI experts, and operations hackers who want to work on breakthrough tech that touches the real world. If you're tired of abstract roadmaps and crave product you can see, taste, and ship—KAIKAKU might be for you.</div>
        </div>
      </div>
    </div>
  </div>
  <div class="mt-8 flex gap-4">
    <a href="/careers" class="btn btn-primary">See open roles</a>
    <a href="mailto:careers@kaikaku.com" class="btn btn-secondary">Start a conversation</a>
  </div>
</div>

	</div>
</section>
