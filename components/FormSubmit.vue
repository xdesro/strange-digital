<template>
  <form class="form-submit">
    <div
      v-for="(fieldset, setName) in fields"
      :key="setName"
      class="form-submit__set"
    >
      <h2 class="form-submit__set-label">{{ setName }}</h2>
      <fieldset class="form-submit__fieldset">
        <div
          v-for="(field, index) in fieldset"
          :key="index + 0"
          :class="{
            'field-group': true,
            'field-group--expanded': field.type === 'textarea'
          }"
        >
          <label :for="field.name" class="field-group__label">
            {{ field.title }}<template v-if="field.required">*</template>
          </label>
          <input
            v-if="field.type !== 'textarea'"
            :type="field.type"
            :name="field.name"
            :required="field.required"
            class="field-group__input"
          />
          <textarea
            v-else
            :name="field.name"
            :required="field.required"
            class="field-group__input field-group__input--textarea"
          />
        </div>
      </fieldset>
    </div>
    <input
      type="submit"
      name="submit"
      value="submit"
      class="form-submit__button"
    />
  </form>
</template>

<script>
export default {
  data() {
    return {
      fields: {
        'Site Details': [
          {
            title: 'Site Name',
            name: 'url',
            required: true,
            type: 'text'
          },
          {
            title: 'Site URL',
            name: 'url',
            required: true,
            type: 'url'
          },
          {
            title: 'Categories',
            name: 'url',
            required: true,
            type: 'text'
          },
          {
            title: 'Tags',
            name: 'url',
            required: true,
            type: 'text'
          },
          {
            title: 'Tech-in-use',
            name: 'url',
            required: false,
            type: 'text'
          }
        ],
        Authorship: [
          {
            title: 'Creator',
            name: 'creator',
            required: true,
            type: 'text'
          },
          {
            title: 'Creator URL',
            name: 'creator-url',
            required: true,
            type: 'url'
          },
          {
            title: 'Social Links',
            name: 'social-links',
            required: false,
            type: 'text'
          },
          {
            title: 'Location',
            name: 'location',
            required: false,
            type: 'text'
          },
          {
            title: 'Additional contributors',
            name: 'additional-contributors',
            required: false,
            type: 'textarea'
          }
        ]
      }
    }
  }
}
</script>

<style lang="scss">
.form-submit {
  grid-row-end: span 2;
  &__set {
    position: relative;
    &:last-of-type {
      margin-bottom: 2rem;
    }
  }
  &__set-label {
    position: absolute;
    text-align: right;
    right: calc(100% + 1.25rem);
    top: 0.75rem;
    white-space: nowrap;
    font-size: 1rem;
    font-family: 'Orelo';
    color: $color__text;
  }
  &__button {
    display: block;
    background: none;
    border: 1px solid $color__accent--primary;
    width: 100%;
    font: inherit;
    color: inherit;
    text-transform: uppercase;
    padding-block: 0.5rem;
    font-weight: 700;
    cursor: pointer;
    &:hover {
      background-color: $color__accent--primary;
      color: $color__background;
    }
  }
}
.field-group {
  $this: &;
  position: relative;
  margin-bottom: 0.4rem;

  &__label {
    position: absolute;
    top: 50%;
    transform: translateY(-50%) scale(1);
    transform-origin: top left;
    transition: transform 0.2s cubic-bezier(0.075, 0.82, 0.165, 1);
    pointer-events: none;
    font-weight: 300;
    #{$this}--expanded & {
      top: 1rem;
    }
  }
  &:focus-within {
    #{$this}__label {
      transform: scale(0.7) translateY(-2rem);
    }
  }
  &__input {
    display: block;
    height: 2.5rem;
    font-size: 1rem;
    width: 100%;
    font-family: inherit;
    border: 0;
    background: none;
    border-bottom: 1px solid $color__accent--primary;
    &--textarea {
      height: 5rem;
    }
  }
}
</style>
