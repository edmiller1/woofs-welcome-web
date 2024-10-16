<template>
  <nav class="bg-background">
    <div class="px-4 mx-auto sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <div class="flex items-center">
          <div class="flex-shrink-0">
            <NuxtLink to="/">
              <span class="flex items-center text-2xl font-bold text-primary">
                <Icon
                  name="lucide:dog"
                  class="w-8 h-8 mr-2 text-primary hover:animate-wiggle"
                />
              </span>
            </NuxtLink>
          </div>
          <div class="hidden md:block">
            <div class="flex items-baseline ml-10 space-x-4">
              <NuxtLink
                to="/List-your-business"
                class="px-3 py-2 text-sm font-semibold rounded-md text-foreground hover:text-primary"
              >
                List your business
              </NuxtLink>
              <NuxtLink
                to="/advertise"
                class="px-3 py-2 text-sm font-semibold rounded-md text-foreground hover:text-primary"
              >
                Advertise
              </NuxtLink>
              <NuxtLink
                to="/about"
                class="px-3 py-2 text-sm font-semibold rounded-md text-foreground hover:text-primary"
              >
                About
              </NuxtLink>
              <NuxtLink
                to="/contact"
                class="px-3 py-2 text-sm font-semibold rounded-md text-foreground hover:text-primary"
              >
                Contact
              </NuxtLink>
              <Button class="font-semibold">Get the app</Button>
            </div>
          </div>
        </div>
        <div class="flex items-center space-x-5 md:hidden">
          <Button>Get the app</Button>
          <Sheet>
            <SheetTrigger asChild>
              <Button
                variant="ghost"
                type="button"
                class="inline-flex items-center justify-center p-1"
              >
                <span class="sr-only">Open main menu</span>
                <Icon name="lucide:menu" class="w-8 h-8" />
              </Button>
            </SheetTrigger>
            <SheetContent side="right" class="flex flex-col">
              <nav class="grid gap-2 text-lg font-medium">
                <div class="flex items-center space-x-2">
                  <Icon name="lucide:dog" class="w-8 h-8 text-primary" />
                  <h1>Woofs Welcome</h1>
                </div>
                <Separator />
                <NuxtLink to="/List-your-business" class="text-foreground">
                  List your business
                </NuxtLink>
                <NuxtLink to="/advertise" class="text-foreground">
                  Advertise
                </NuxtLink>
                <NuxtLink to="/about" class="text-foreground"> About </NuxtLink>
                <NuxtLink to="/contact" class="text-foreground">
                  Contact
                </NuxtLink>
              </nav>
              <div class="mt-auto">
                <Button class="w-full">Log in</Button>
              </div>
            </SheetContent>
          </Sheet>
        </div>
        <div class="items-center hidden space-x-4 md:flex">
          <Button asChild class="font-semibold">
            <NuxtLink to="/login"> Log in </NuxtLink>
          </Button>
          <Button variant="link" class="font-semibold text-black"
            ><NuxtLink to="/signup">Create account &rarr;</NuxtLink></Button
          >
        </div>
        <!-- <div class="flex items-center justify-end w-full space-x-5 md:hidden">
        {currentProfile ? (
          <>
            <Link href="/notifications">
              <Button class="rounded-full px-1.5">
                <Bell />
              </Button>
            </Link>
            <UserMenu currentProfile={currentProfile} />
          </>
        ) : (
          <Button>
            <Link href="/login">Log in</Link>
          </Button>
        )}
      </div> -->
      </div>
    </div>
  </nav>
</template>
