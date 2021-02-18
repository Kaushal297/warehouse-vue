<template>
  <div class="about">
    <div class="container">
      <h2 class="text-align-center">Warehouse Details</h2>
      <div>
        <button>
          <svg viewBox="0 0 477.873 477.873" class="edit-icon">
            <path
              d="M392.533,238.937c-9.426,0-17.067,7.641-17.067,17.067V426.67c0,9.426-7.641,17.067-17.067,17.067H51.2 c-9.426,0-17.067-7.641-17.067-17.067V85.337c0-9.426,7.641-17.067,17.067-17.067H256c9.426,0,17.067-7.641,17.067-17.067 S265.426,34.137,256,34.137H51.2C22.923,34.137,0,57.06,0,85.337V426.67c0,28.277,22.923,51.2,51.2,51.2h307.2	c28.277,0,51.2-22.923,51.2-51.2V256.003C409.6,246.578,401.959,238.937,392.533,238.937z"
            />
            <path
              d="M458.742,19.142c-12.254-12.256-28.875-19.14-46.206-19.138c-17.341-0.05-33.979,6.846-46.199,19.149L141.534,243.937 c-1.865,1.879-3.272,4.163-4.113,6.673l-34.133,102.4c-2.979,8.943,1.856,18.607,10.799,21.585 c1.735,0.578,3.552,0.873,5.38,0.875c1.832-0.003,3.653-0.297,5.393-0.87l102.4-34.133c2.515-0.84,4.8-2.254,6.673-4.13 l224.802-224.802C484.25,86.023,484.253,44.657,458.742,19.142z M434.603,87.419L212.736,309.286l-66.287,22.135l22.067-66.202 L390.468,43.353c12.202-12.178,31.967-12.158,44.145,0.044c5.817,5.829,9.095,13.72,9.12,21.955 C443.754,73.631,440.467,81.575,434.603,87.419z"
            />
          </svg>
        </button>
      </div>
      <form action="" method="">
        <div class="table-view">
          <p>cluster</p>
          <p>
            <input type="text" name="cluster" value="cluster-a-32" disabled />
          </p>
        </div>
        <div class="table-view">
          <p>warehouse name</p>
          <p>
            <input type="text" name="arehouse" value="Warehouse-165" disabled />
          </p>
        </div>
        <div class="table-view">
          <p>city</p>
          <p><input type="text" name="Delhi" value="Delhi" disabled /></p>
        </div>
        <div class="table-view">
          <p>space available</p>
          <p><input type="text" name="1234" value="1234" disabled /></p>
        </div>
        <div class="table-view">
          <p>warehouse live status</p>
          <p><input type="text" name="false" value="false" disabled /></p>
        </div>
        <input type="submit" name="submit" />
      </form>
    </div>
  </div>
</template>

<style scoped>
.container {
  width: 30%;
  margin: 0 35%;
}

.table-view {
  display: flex;
  justify-content: space-evenly;
  border: 1px solid black;
  padding: 10px;
}

.table-view p {
  width: 50%;
  padding: 10px;
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

.edit-icon {
  cursor: pointer;
  fill: red;
}
</style>
