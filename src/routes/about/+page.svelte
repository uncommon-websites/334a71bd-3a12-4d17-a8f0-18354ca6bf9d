<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Innovation",
			description: "Constantly challenging the status quo to create better solutions."
		},
		{
			title: "Integrity",
			description: "Building trust through transparent actions and honest communication."
		},
		{
			title: "Impact",
			description: "Measuring our success by the positive change we create for our clients."
		}
	];
</script>

<SecondaryHero
	title="Solving world hunger"
	subtitle="one step at a time"
	imageSrc="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1471&q=80"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"We started in 2018 with a simple goal: make helpful tech that people actually need. While many chase profits, we chose to do things differently.",
		"Beyond making good products, we care about doing the right thing, being kind to our planet, and making sure everyone can use what we build. That's our compass.",
		"From day one, we've asked ourselves: 'Does this actually help people?' This question gets us through tough calls and shapes who we are. We're playing the long game here.",
		"We think about how our work affects real people's lives. We build tech that brings people together, keeps your information safe, and treats everyone fairly. When we stick to these basics, good things happen."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Our founder."
  subtitle="Building the future of restaurants from London."
  stakeholders={[
    {
      name: "Josef Chen",
      position: "Founder & CEO",
      bio: "Josef Chen is the founder and CEO of KAIKAKU, where he leads product and company vision for the operating system modernizing restaurants through robotics and AI. As a relentless builder and systems thinker, Josef is committed to solving the toughest operational challenges in food service while championing exceptional guest experiences. With deep roots in both technology and hospitality, he is rewriting how restaurants run—faster, smarter, and with limitless personalization.",
      image: "/generated/image-a-professional-headshot-of-an-asian-man-.webp"
    }
  ]}
/>




<!-- CTA Section -->
<CallToAction
	title="Join us and build what's next"
	subtitle="Help shape the future of food"
	description="KAIKAKU is hiring bold engineers, operators, and hospitality leaders to reinvent restaurant tech from the ground up. If you’re looking for meaningful ownership, high-impact work, and a chance to build real systems for the real world—we’d like to meet you."
	imageSrc="/generated/image-a-lively-scene-in-a-contemporary-restaur.webp"
	callsToAction={[
    { href: "/careers", label: "Explore open roles", variant: "primary" },
    { href: "mailto:careers@kaikaku.io", label: "Reach out directly", variant: "secondary" }
  ]}
/>
