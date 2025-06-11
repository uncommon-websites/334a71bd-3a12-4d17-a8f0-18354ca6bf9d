<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
	{
		title: "Early builder",
		description: "Shape the future of robotics and AI in restaurants as part of our founding team. Your work directly affects real-world customers and operations.",
		icon: IconBriefcase
	},
	{
		title: "Extreme ownership",
		description: "Take direct responsibility for your projects with support from top engineers and direct feedback from leadership. Radically transparent and meritocratic environment.",
		icon: IconUsers
	},
	{
		title: "Next-level growth",
		description: "Accelerate your learning building across hardware, software, and operations. Stock options, top-tier benefits, and the chance to solve the QSR industry's hardest problems.",
		icon: IconHeart
	}
];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Lina Zhang",
    position: "Junior Robotics Engineer",
    company: "Engineering Team",
    quote:
      "From day one, my teammates and mentors have pushed me to learn by doing. There’s no ego—just lots of curiosity and teamwork. Building next-gen robotics, I feel included, supported, and constantly challenged. It’s inspiring to see your ideas come to life so quickly.",
    image: "/generated/image-an-asian-woman-engineer-in-a-contemporar.webp"
  },
  {
    name: "Daryl Thompson",
    position: "Operations Manager",
    company: "Operations Team",
    quote:
      "At KAIKAKU, it’s not just about automation—it’s about creating impact. I joined as a supervisor and worked my way up. Leadership here invests in you, listens to every voice, and champions diversity. I feel valued every day, and my growth has been incredible.",
    image: "/generated/image-a-black-man-working-as-an-operations-man.webp"
  },
  {
    name: "Taylor Brooks",
    position: "Product Designer",
    company: "Product Team",
    quote:
      "This is the most open and creative environment I’ve ever worked in. I can shape real products that blend AI, robotics, and design—alongside people who care deeply about inclusion and learning. No two days are the same, and I’ve grown so much as a designer and as a person.",
    image: "/generated/image-a-white-nonbinary-product-designer-in-a-.webp"
  }
];

	const processSteps = [
	{
		step: 1,
		title: "Apply",
		description: "Send us your CV or portfolio and tell us briefly why you want to help build the future of restaurants. Everyone gets a direct response."
	},
	{
		step: 2,
		title: "Team interview",
		description: "Meet our founders and technical leads for an in-depth discussion about your experience, values, and problem-solving skills."
	},
	{
		step: 3,
		title: "Paid challenge",
		description: "Take on a short, real-world project or technical challenge relevant to the role. We pay you for your time and give actionable feedback."
	},
	{
		step: 4,
		title: "Offer & onboarding",
		description: "If we're a mutual fit, you'll receive your offer quickly and we'll get you set up for a fast, impactful start." 
	}
];

	const values = [
	{
		icon: IconHeart,
		title: "First-principles mindset",
		description: "We solve tough problems from the ground up and never follow the industry playbook by default."
	},
	{
		icon: IconUsers,
		title: "Radical ownership",
		description: "Everyone is responsible for outcomes. We win together and push each other to move fast and iterate forward."
	},
	{
		icon: IconGlobe,
		title: "No egos, just impact",
		description: "We hire for curiosity, learn from every background, give and get feedback often, and drive progress over politics."
	}
];
</script>

<!-- Hero Section -->

<SecondaryHero
	title="Build with AI. Serve the future."
	subtitle="Join a mission-driven team using robotics and intelligence to transform how the world eats—together."
	imageSrc="/generated/image-a-diverse-group-of-young-professionals-i.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
