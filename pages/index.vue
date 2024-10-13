<template>
  <section
    class="flex flex-col w-full min-h-screen bg-background overflow-x-none"
  >
    <Navbar />
    <div class="items-center justify-center flex-1 px-4 py-10 lg:flex lg:px-10">
      <div class="flex flex-col p-4 mb-5 space-y-4 mg:mb-0 lg:w-1/2">
        <h1 class="text-6xl font-bold tracking-tighter">
          Explore and discover New Zealand's
          <span class="font-extrabold text-primary">dog-friendly</span>
          places.
        </h1>
        <p class="text-gray-500 md:w-2/3">
          Looking for the perfect spot to explore with your furry best friend?
          Our website is your go-to guide for all things dog-friendly in New
          Zealand. From scenic hikes and cozy cafes to dog-friendly beaches and
          accommodation, we've got you covered. Find your next adventure
          together!
        </p>
        <div class="flex justify-start">
          <Button asChild>
            <Link href="/login">Start exploring</Link>
          </Button>
        </div>
      </div>
      <div
        class="hidden w-full mr-20 space-x-5 lg:flex lg:justify-end lg:space-x-10 lg:w-1/2"
      >
        <div class="lg:pt-80">
          <div class="relative">
            <NuxtImg
              src="https://images.unsplash.com/photo-1532592333381-a141e3f197c9?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTJ8fGRvZ3xlbnwwfHwwfHx8MA%3D%3D"
              alt="Dog"
              class="hidden object-cover object-center w-48 rounded-lg shadow-xl h-72 md:block"
            />
          </div>
        </div>
        <div class="flex flex-col pt-36 lg:space-y-5">
          <div class="relative">
            <NuxtImg
              src="https://images.unsplash.com/photo-1636152253795-3d87eb8bd7da?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NTV8fGRvZyUyMHBhcmt8ZW58MHx8MHx8fDA%3D"
              alt="Dog"
              class="object-cover object-center rounded-lg shadow-xl h-72 md:w-48"
            />
          </div>
          <div class="relative">
            <NuxtImg
              src="https://images.unsplash.com/photo-1557199582-14cd70bc6d39?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8N3x8ZG9nJTIwY2l0eXxlbnwwfHwwfHx8MA%3D%3D"
              alt="Dog"
              class="object-cover object-center rounded-lg shadow-xl h-72 md:w-48"
            />
          </div>
        </div>
        <div class="flex flex-col space-y-5">
          <div class="relative">
            <NuxtImg
              src="https://images.unsplash.com/photo-1579981581825-15f100307b78?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8ZG9nJTIwZXhwbG9yZXxlbnwwfHwwfHx8MA%3D%3D"
              alt="Dog"
              class="object-cover object-center rounded-lg shadow-xl h-72 md:w-48"
            />
          </div>
          <div class="relative">
            <NuxtImg
              src="https://images.unsplash.com/photo-1704361469172-1329069f0a29?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fGRvZyUyMGJlYWNofGVufDB8fDB8fHww"
              alt="Dog"
              class="object-cover object-center rounded-lg shadow-xl h-72 md:w-48"
            />
          </div>
        </div>
      </div>
      <div class="grid grid-cols-2 gap-4 lg:hidden">
        <NuxtImg
          src="https://images.unsplash.com/photo-1636152253795-3d87eb8bd7da?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NTV8fGRvZyUyMHBhcmt8ZW58MHx8MHx8fDA%3D"
          alt="Dog"
          class="object-cover object-center w-full h-48 rounded-lg shadow-xl"
        />
        <NuxtImg
          src="https://images.unsplash.com/photo-1532592333381-a141e3f197c9?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTJ8fGRvZ3xlbnwwfHwwfHx8MA%3D%3D"
          alt="Dog"
          class="object-cover object-center w-full h-48 rounded-lg shadow-xl"
        />
        <NuxtImg
          src="https://images.unsplash.com/photo-1579981581825-15f100307b78?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8ZG9nJTIwZXhwbG9yZXxlbnwwfHwwfHx8MA%3D%3D"
          alt="Dog"
          class="object-cover object-center w-full h-48 rounded-lg shadow-xl"
        />
        <NuxtImg
          src="https://images.unsplash.com/photo-1704361469172-1329069f0a29?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fGRvZyUyMGJlYWNofGVufDB8fDB8fHww"
          alt="Dog"
          class="object-cover object-center w-full h-48 rounded-lg shadow-xl"
        />
      </div>
    </div>
    <section class="flex flex-col py-12 lg:flex-row bg-muted lg:px-44 lg:py-24">
      <div
        class="flex flex-col justify-center lg:flex-row lg:items-center lg:space-x-32"
      >
        <Carousel class="px-5 lg:w-3/4">
          <CarouselContent>
            <CarouselItem>
              <div
                class="grid w-full grid-cols-2 gap-x-2 gap-y-3 lg:grid-cols-3"
              >
                <div
                  v-for="type in firstTypes"
                  :key="type.title"
                  class="relative"
                >
                  <NuxtImg
                    :src="type.image"
                    alt="Dog"
                    class="object-cover object-center w-56 h-40 rounded-lg shadow-xl brightness-75"
                  />
                  <span
                    class="absolute text-lg font-semibold text-white bottom-3 left-3"
                  >
                    {{ type.title }}
                  </span>
                </div>
              </div>
            </CarouselItem>
            <CarouselItem>
              <div
                class="grid w-full grid-cols-2 gap-x-2 gap-y-3 lg:grid-cols-3"
              >
                <div
                  v-for="type in secondTypes"
                  :key="type.title"
                  class="relative"
                >
                  <NuxtImg
                    :src="type.image"
                    alt="Dog"
                    class="object-cover object-center w-56 h-40 rounded-lg shadow-xl brightness-75"
                  />
                  <span
                    class="absolute text-lg font-semibold text-white bottom-3 left-3"
                  >
                    {{ type.title }}
                  </span>
                </div>
              </div>
            </CarouselItem>
          </CarouselContent>
          <CarouselPrevious class="hidden lg:flex lg:items-center" />
          <CarouselNext class="hidden lg:flex lg:items-center" />
        </Carousel>
      </div>
      <div class="px-5 lg:w-3/4">
        <h2 class="mt-5 text-5xl font-bold">
          Plenty of dog-friendly places to explore
        </h2>
        <p class="mt-5 text-gray-500">
          From scenic hikes and cozy cafes to dog-friendly beaches and
          accommodations. Find your next adventure together!
        </p>
      </div>
    </section>
    <Footer />
  </section>
</template>
