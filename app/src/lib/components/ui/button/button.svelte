<script lang="ts">
import { Button as ButtonPrimitive } from "bits-ui"
import { type Events, type Props, buttonVariants } from "./index.js"
import { cn } from "$lib/utilities/shadcn.js"

type $$Props = Props
type $$Events = Events

let className: $$Props["class"] = undefined
export let value: $$Props["value"] = ""
export let variant: $$Props["variant"] = "default"
export let size: $$Props["size"] = "default"
export let builders: $$Props["builders"] = []
export let name: $$Props["name"] = "button"
export let disabled: $$Props["disabled"] = false
export { className as class }
</script>

<ButtonPrimitive.Root
  {name}
  {builders}
  {disabled}
  class={cn(buttonVariants({ variant, size, className }))}
  type="button"
  {...$$restProps}
  on:click
  on:keydown
>
  <slot>
    {value}
  </slot>
</ButtonPrimitive.Root>
