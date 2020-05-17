<template>
  <nav class="main-nav">
    <div class="main-nav__head">
      <div class="main-nav__inner">
        <nav-toggle text="Породы" @open-nav="navIsOpen = !navIsOpen" />
        <div class="main-nav__current">
          <nav-item-current />
        </div>
      </div>
      <sort-toggle text="Сортировка по алфавиту" />
    </div>
    <div class="main-nav__body">
      <transition name="fade">
        <nav-list v-if="navIsOpen" text-all="Все пёсели" :list="sortedList" />
      </transition>
    </div>
  </nav>
</template>

<script>
import NavToggle from "@/components/NavToggle";
import NavList from "@/components/NavList";
import NavItemCurrent from "@/components/NavItemCurrent";
import SortToggle from "@/components/SortToggle";

export default {
  name: "TheNav",
  components: {
    NavToggle,
    SortToggle,
    NavList,
    NavItemCurrent
  },
  data() {
    return {
      navIsOpen: false,
      list: {
        affenpinscher: [],
        african: [],
        airedale: [],
        akita: [],
        appenzeller: [],
        australian: ["shepherd"],
        basenji: [],
        beagle: [],
        bluetick: [],
        borzoi: [],
        bouvier: [],
        boxer: [],
        brabancon: [],
        briard: [],
        buhund: ["norwegian"],
        bulldog: ["boston", "english", "french"],
        bullterrier: ["staffordshire"],
        cairn: [],
        cattledog: ["australian"],
        chihuahua: [],
        chow: [],
        clumber: [],
        cockapoo: [],
        collie: ["border"],
        coonhound: [],
        corgi: ["cardigan"],
        cotondetulear: [],
        dachshund: [],
        dalmatian: [],
        dane: ["great"],
        deerhound: ["scottish"],
        dhole: [],
        dingo: [],
        doberman: [],
        elkhound: ["norwegian"],
        entlebucher: [],
        finnish: ["lapphund"],
        frise: ["bichon"],
        germanshepherd: [],
        greyhound: ["italian"],
        groenendael: [],
        havanese: [],
        hound: [
          "afghan",
          "basset",
          "blood",
          "english",
          "ibizan",
          "plott",
          "walker"
        ],
        husky: [],
        keeshond: [],
        kelpie: [],
        komondor: [],
        kuvasz: [],
        labrador: [],
        leonberg: [],
        lhasa: [],
        malamute: [],
        malinois: [],
        maltese: [],
        mastiff: ["bull", "english", "tibetan"],
        mexicanhairless: [],
        mix: [],
        mountain: ["bernese", "swiss"],
        newfoundland: [],
        otterhound: [],
        ovcharka: ["caucasian"],
        papillon: [],
        pekinese: [],
        pembroke: [],
        pinscher: ["miniature"],
        pitbull: [],
        pointer: ["german", "germanlonghair"],
        pomeranian: [],
        poodle: ["miniature", "standard", "toy"],
        pug: [],
        puggle: [],
        pyrenees: [],
        redbone: [],
        retriever: ["chesapeake", "curly", "flatcoated", "golden"],
        ridgeback: ["rhodesian"],
        rottweiler: [],
        saluki: [],
        samoyed: [],
        schipperke: [],
        schnauzer: ["giant", "miniature"],
        setter: ["english", "gordon", "irish"],
        sheepdog: ["english", "shetland"],
        shiba: [],
        shihtzu: [],
        spaniel: [
          "blenheim",
          "brittany",
          "cocker",
          "irish",
          "japanese",
          "sussex",
          "welsh"
        ],
        springer: ["english"],
        stbernard: [],
        terrier: [
          "american",
          "australian",
          "bedlington",
          "border",
          "dandie",
          "fox",
          "irish",
          "kerryblue",
          "lakeland",
          "norfolk",
          "norwich",
          "patterdale",
          "russell",
          "scottish",
          "sealyham",
          "silky",
          "tibetan",
          "toy",
          "westhighland",
          "wheaten",
          "yorkshire"
        ],
        vizsla: [],
        waterdog: ["spanish"],
        weimaraner: [],
        whippet: [],
        wolfhound: ["irish"]
      }
    };
  },
  computed: {
    sortedList() {
      return Object.keys(this.list).sort();
    }
  }
};
</script>
