<script setup>
import SiteHeader from "./components/SiteHeader.vue"
import Gallery from "./components/Gallery.vue"
import Portfolio from "./components/Portfolio.vue"

// data to populate the portfolio
// id: element id to link gallery images to a project heading
// title: text for the project heading
// text: companion text for the project section
// images: images to display in the project section, plus alt text
//     the first image will be displayed in the gallery
const projects = [
    {
        id: "street",
        title: "Street",
        text: [
            `This concept is based around a witch living
            in the city with her crow familiar. Her
            rowhouse is older and more ornate than the
            others on the block, with decorations
            styled to look like feathers and wings.`
        ],
        images: [
            {src: "street lines.jpg", alt: "A drawing of a block of rowhouses with an ornate Victorian house in the center. Skyscrapers rise behind the houses, and the scene is framed by a pair of tree trunks in the foreground."}
        ]
    },
    {
        id: "treasure",
        title: "Treasure",
        text: [
            `I designed and painted this background as
                part of a short collaborative film called
                Beneath the Dungeon for my school’s intro
                animation class. It’s based on a storyboard by
                the teacher, Anthony Gardea. Our hero is a
                young boy trying to swipe a soda his older
                brother has been saving. He imagines he’s
                venturing into a treacherous dungeon and
                grabbing it from a huge treasure chest, which
                is really the fridge in his basement.`
        ],
        images: [
            {src: "treasure paint.jpg", alt: "A painting of a large treasure chest in a vast dungeon hall, surrounded by piles of gold. A skeleton sits leaning against the right side of the chest clutching at a sword between its ribs."},
            {src: "treasure lines.jpg", alt: "A drawing of a large treasure chest in a vast dungeon hall, surrounded by piles of gold. A skeleton sits leaning against the right side of the chest clutching at a sword between its ribs."}
        ]
    },
    {
        id: "potion",
        title: "Potion",
        text: [
            `This background is from the same student
                film, Beneath the Dungeon, as Treasure. For
                this one I started with some prop sketches
                which supplied most of the wizardy clutter in
                the frame.`
        ],
        images: [
            {src: "potion paint.jpg", alt: "A painting of a potion bottle with a label reading \"Dont touch\" on a wooden background, surrounded by cluttered books, bottles, candles and other arcane implements."},
            {src: "potion lines.jpg", alt: "A drawing of a potion bottle with a label reading \"Dont touch\" on a wooden background, surrounded by cluttered books, bottles, candles and other arcane implements."},
            {src: "potion props.jpg", alt: "Drawings of assorted bottles, candles and other items."}
        ]
    },
    {
        id: "creek",
        title: "Creek",
        text: [
            `To make this illustration of a house in
                the countryside, I drew a kit with trees,
                rocks and shrubs, then used it to build up
                the scene around this Victorian cottage.`
        ],
        images: [
            {src: "creek lines.jpg", alt: "A drawing of a Victorian cottage next to a willow tree in the woods, with a creek running through the foreground to the left."},
            {src: "creek kit.jpg", alt: "Drawings of assorted trees, rocks and shrubs."}
        ]
    },
    {
        id: "faerie",
        title: "Faerie Borough",
        text: [
            `This storyboard is a cold open for a cartoon
                about magical weirdos far from home, stuck
                running a New York City bodega in the human
                world.`
        ],
        images: [
            {src: "fb edda broom.jpg", alt: "A cartoon of a witch looking over her shoulder. Her hat and broom are lying on the floor in front of a pile of boxes."},
            {src: "fb edda bobble.jpg", alt: "A cartoon of a witch, left, shouting in anger and a goblin, right, looking bemused, raising one eyebrow."},
            {src: "fb soda.jpg", alt: "A cartoon looking down towards a man reaching for a bottle of soda on a high shelf in the foreground."}
        ]
    },
    {
        id: "ngon",
        title: "Ngon Outlaw",
        text: [
            `For this short car chase scene I started
                by drawing beat boards on paper, then modeled
                environments in Blender and animated camera
                movements, vehicles and effects. I used Synty
                Studios’ sci-fi city asset pack to quickly
                layout these scenes in 3d.`
        ],
        images: [
            {src: "frame0064.jpg", alt: "A 3d render of a flying car chased by a cop with a futuristic city in the background."},
            {src: "frame0361.jpg", alt: "A 3d render of a flying car chased by a cop, weaving through traffic in a highway tunnel."}
        ]
    }
]

// get a list of all the images used for each project
// will use this for the slideshow modal
const images = projects.reduce((imgList, proj) => imgList.concat(proj.images), [])
</script>

<template>
    <SiteHeader />
    <Gallery :projects="projects" />
    <Portfolio :projects="projects" />
</template>

<style scoped>
</style>
