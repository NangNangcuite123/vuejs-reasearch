<template>
  <div class="row">
    <div class="col-4">
      <div class="card">
        <slot name="header"></slot> <!-- Named Slot -->
        <slot></slot> <!-- default slot -->
        <slot name="footer"></slot><!-- Named Slot -->
      </div>
    </div>
    <div class="col-4">
      <div class="card">
        <slot name="header"></slot><!-- Named Slot -->
        <slot></slot> <!-- default slot -->
        <slot name="footer"></slot><!-- Named Slot -->
      </div>
    </div>
    <div class="col-4">
      <div class="card">
        <slot name="header"></slot><!-- Named Slot -->
        <slot></slot> <!-- default slot -->
        <slot name="footer"></slot><!-- Named Slot -->
      </div>
    </div>
  </div>
</template>
