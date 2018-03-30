<template>

  <div class="note">
    <a href="#" class="note__delete">
      <span class="note__delete-icon">&times;</span>
    </a>
    <div class="note__content">
      <a href="#" class="note__title">Note one</a>
      <p class="note__body">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi facere fugit inventore magni.</p>
    </div>
  </div>

</template>

<script>
  export default {

  }
</script>

<style lang="scss" scoped>
  .note {
    display: flex;
    color: inherit;
    text-decoration: none;
    border-bottom: 2px solid #eee;
    opacity: .6;
    flex-direction: row;
    max-width: 100%;

    &:hover {
      opacity: 1;

      .note__delete {
        margin-left: 0;
      }
    }

    &__content {
      padding: 30px;
      flex: 2;
      overflow: hidden;
    }

    &__title {
      display: block;
      font-size: 1em;
      margin: 0;
      font-weight: 500;
      text-decoration: none;
      color: inherit;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;

      &:hover {
        text-decoration: underline;
      }
    }

    &__body {
      font-size: .9em;
      margin-bottom: 0;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }

    &__delete {
      position: relative;
      margin-left: -50px;
      width: 50px;
      display: block;
      background: #cc4466;
      min-height: 100%;
      color: #fff;
      transition: 100ms margin-left ease-in-out;
    }

    &__delete-icon {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 1.5em;
      font-weight: 600;
    }
  }
</style>
