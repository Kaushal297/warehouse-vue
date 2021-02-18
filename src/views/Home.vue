<template>
  <div class="home">
    <div>
      <div class="flex-jc-cntr">
        <div class="search-box">
          <input
            type="search"
            name="search"
            placeholder="Search for warehouse"
          />
          <button>
            <svg viewBox="0 0 512.005 512.005" class="search-icon">
              <path
                d="M505.749,475.587l-145.6-145.6c28.203-34.837,45.184-79.104,45.184-127.317c0-111.744-90.923-202.667-202.667-202.667 S0,90.925,0,202.669s90.923,202.667,202.667,202.667c48.213,0,92.48-16.981,127.317-45.184l145.6,145.6 c4.16,4.16,9.621,6.251,15.083,6.251s10.923-2.091,15.083-6.251C514.091,497.411,514.091,483.928,505.749,475.587z M202.667,362.669c-88.235,0-160-71.765-160-160s71.765-160,160-160s160,71.765,160,160S290.901,362.669,202.667,362.669z"
              />
            </svg>
          </button>
        </div>
        <div class="text-align-center">
          <button class="filter-btn">
            <svg viewBox="-4 0 393 393.99003">
              <path
                d="m368.3125 0h-351.261719c-6.195312-.0117188-11.875 3.449219-14.707031 8.960938-2.871094 5.585937-2.3671875 12.3125 1.300781 17.414062l128.6875 181.28125c.042969.0625.089844.121094.132813.183594 4.675781 6.3125 7.203125 13.957031 7.21875 21.816406v147.796875c-.027344 4.378906 1.691406 8.582031 4.777344 11.6875 3.085937 3.105469 7.28125 4.847656 11.65625 4.847656 2.226562 0 4.425781-.445312 6.480468-1.296875l72.3125-27.574218c6.480469-1.976563 10.78125-8.089844 10.78125-15.453126v-120.007812c.011719-7.855469 2.542969-15.503906 7.214844-21.816406.042969-.0625.089844-.121094.132812-.183594l128.683594-181.289062c3.667969-5.097657 4.171875-11.820313 1.300782-17.40625-2.832032-5.511719-8.511719-8.9726568-14.710938-8.960938zm-131.53125 195.992188c-7.1875 9.753906-11.074219 21.546874-11.097656 33.664062v117.578125l-66 25.164063v-142.742188c-.023438-12.117188-3.910156-23.910156-11.101563-33.664062l-124.933593-175.992188h338.070312zm0 0"
              />
            </svg>
          </button>
        </div>
      </div>
      <div>
        <div class="container">
          <div
            v-for="warehouseitem in warehouse"
            :key="warehouseitem.id"
            class="contrainer-item"
          >
            <p>{{ warehouseitem.name }}</p>
            <p>{{ warehouseitem.city }}</p>
            <p>{{ warehouseitem.cluster }}</p>
            <p>{{ warehouseitem.is_live }}</p>
          </div>
        </div>
      </div>
    </div>

    <div>
      <p></p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data: () => ({
    warehouse: []
  }),
  mounted() {
    this.warehouse = this.$store.getters.getAllWarehouse;
  }
};
</script>

<style scoped>
.search-box {
  display: flex;
  justify-content: space-between;
  width: 50%;
  border: 1px solid blue;
  padding: 5px;
  border-radius: 25px;
}

input {
  flex-grow: 100;
  margin-right: 10px;
  border: none;
  font-size: 16px;
  margin-left: 20px;
}

input:focus {
  outline: none;
}

button {
  width: 30px;
  background-color: #fff;
  border: none;
  padding: 5px;
  flex-grow: 1;
  margin-right: 10px;
  outline: none;
}

.search-icon {
  cursor: pointer;
  fill: #2874f0;
  margin: 0;
}

/* container for list of warehouse */
.container {
  margin-top: 50px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.contrainer-item {
  text-align: center;
  width: calc(100% / 5);
  border: 1px solid red;
  border-radius: 25px;
  padding: 10px;
  margin: 0 20px 20px 20px;
  cursor: pointer;
}

/* filter button */
.filter-btn {
  cursor: pointer;
  fill: rgb(129, 235, 9);
  outline: none;
}
</style>
