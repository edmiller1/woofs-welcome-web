<script setup lang="ts">
import { useForm } from "vee-validate";

import { toTypedSchema } from "@vee-validate/zod";
import * as z from "zod";
import { toast } from "vue-sonner";

const signUpLoading = ref(false);

const redirectTo = `${useRuntimeConfig().public.baseUrl}/confirm`;

const formSchema = toTypedSchema(
  z.object({
    businessName: z
      .string()
      .min(1, { message: "Business name is required" })
      .max(50),
    contactName: z
      .string()
      .min(1, { message: "Contact name is required" })
      .max(50),
    email: z.string().email(),
    password: z.string().min(8),
  })
);

const form = useForm({
  validationSchema: formSchema,
});

const onSubmit = form.handleSubmit(async (values) => {
  signUpLoading.value = false;
  console.log("Form submitted!", values);
});
</script>

<template>
  <div class="flex flex-col w-full min-h-screen bg-background">
    <nav class="p-4">
      <NuxtLink to="/">
        <span class="flex items-center text-2xl font-bold text-primary">
          <Icon
            name="lucide:dog"
            class="w-8 h-8 mr-2 text-primary hover:animate-wiggle"
          />
        </span>
      </NuxtLink>
    </nav>
    <div
      class="flex flex-col justify-center flex-1 min-h-full py-8 sm:px-6 lg:px-8"
    >
      <Card class="max-w-sm mx-auto">
        <CardHeader>
          <CardTitle class="text-2xl"> Sign Up </CardTitle>
          <CardDescription>
            Enter your details below to create an account
          </CardDescription>
        </CardHeader>
        <CardContent>
          <form @submit.prevent="onSubmit">
            <div class="grid gap-4">
              <FormField
                v-slot="{ componentField }"
                name="businessName"
                class="grid gap-2"
              >
                <FormItem>
                  <FormLabel>Business Name</FormLabel>
                  <FormControl>
                    <Input type="text" v-bind="componentField" />
                  </FormControl>
                  <FormMessage />
                </FormItem>
              </FormField>
              <FormField
                v-slot="{ componentField }"
                name="contactName"
                class="grid gap-2"
              >
                <FormItem>
                  <FormLabel>Contact Name</FormLabel>
                  <FormControl>
                    <Input type="text" v-bind="componentField" />
                  </FormControl>
                  <FormMessage />
                </FormItem>
              </FormField>
              <FormField
                v-slot="{ componentField }"
                name="email"
                class="grid gap-2"
              >
                <FormItem>
                  <FormLabel>Email</FormLabel>
                  <FormControl>
                    <Input type="email" v-bind="componentField" />
                  </FormControl>
                  <FormMessage />
                </FormItem>
              </FormField>
              <FormField
                v-slot="{ componentField }"
                name="password"
                class="grid gap-2"
              >
                <FormItem>
                  <FormLabel>Password</FormLabel>
                  <FormControl>
                    <Input type="password" v-bind="componentField" />
                  </FormControl>
                  <FormMessage />
                </FormItem>
              </FormField>
              <Button v-if="signUpLoading" class="w-full" disabled>
                <Icon
                  name="lucide:loader-circle"
                  class="w-4 h-4 mr-2 animate-spin"
                />
                Signing up
              </Button>
              <Button v-else type="submit" class="w-full"> Sign up </Button>
            </div>
            <div class="mt-4 text-sm text-center">
              Already have a business account?
              <NuxtLink to="#" class="underline"> Log in </NuxtLink>
            </div>
          </form>
        </CardContent>
      </Card>
    </div>
  </div>
</template>
