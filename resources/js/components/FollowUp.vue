<template>
  <portal to="modals">
    <transition name="fade">
      <modal v-if="openModal" @modal-close="openModal = false">
        <div
          class="bg-white rounded-lg shadow-lg overflow-hidden"
          style="width: 460px"
        >
          <div class="p-8">
            <heading
              :level="2"
              class="mb-6"
            >
            test heading
            </heading>
            <p class="text-80 leading-normal">
                test paragraph
            </p>
          </div>
          <div
            class="border-t border-50 px-6 py-3 ml-auto flex items-center"
            style="min-height: 70px; flex-direction: row-reverse"
          >
            <a
              style="order: 2"
              class="cursor-pointer btn text-80 font-normal px-3 mr-3 btn-link"
              @click.prevent="openModal = false"
              >Cancel</a
            >
          </div>
        </div>
      </modal>
    </transition>
  </portal>
</template>
<script>
export default {
    data() {
        return {
            openModal: false
        }
    }
}
</script>