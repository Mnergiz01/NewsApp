<template>
    <div class="grid grid-cols-2 gap-6 p-6">
        <!-- Sol Sütun -->
        <div class="flex flex-col gap-5">
            <!-- Üstteki Büyük Görsel -->
            <div>
                <img src="@/assets/biden.png" alt="Main Image" class="w-full h-full object-cover rounded-xl shadow" />
            </div>

            <!-- Başlık ve Açıklama + Küçük Görsel -->
            <div class="flex gap-5 mt-10">
                <div class="flex-1">
                    <h2 class="text-xl font-bold mb-2">Philomena Cunk Is Weird Enough to Take on the World</h2>
                    <p class="text-sm text-gray-700">
                        The new Netflix show “Cunk on Earth” looks like an ambitious BBC documentary. Until its
                        fictional host, created by Charlie Brooker, starts to ask some deeply silly questions.
                    </p>
                </div>
                <div class="w-32 flex items-end">
                    <img src="@/assets/1.png" alt="Side Image" class="w-full object-contain" />
                </div>
            </div>
        </div>

        <!-- Sağ Sütun -->
        <div class="grid grid-rows-3 gap-4">
            <!-- Üstteki İki Satırı Kapsayan Alan -->
            <div class="row-span-2 bg-gray-900 text-white rounded-xl overflow-hidden shadow">
                <div class="grid grid-cols-2 h-full">
                    <!-- Sol içerik -->
                    <div class="p-4 flex items-center">
                        <p class="text-sm">
                            Secretary of State Antony J. Blinken on Friday canceled a weekend trip to Beijing after a
                            Chinese spy
                            balloon was sighted above the Rocky Mountain state of Montana, igniting a frenzy of media
                            coverage and
                            political commentary over a machine that the Pentagon said posed no threat to the United
                            States.
                        </p>
                    </div>

                    <!-- Sağ görsel ve başlık -->
                    <div class="relative flex items-center justify-center p-2">
                        <img src="@/assets/2.png" alt="Side Image" class="w-full h-full object-cover rounded-xl" />
                        <div class="absolute bottom-4 px-3 py-2 rounded">
                            <h1 class="text-white text-xl font-semibold">
                                Furor Over Chinese Spy Balloon Leads to a Diplomatic Crisis
                            </h1>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Alt Satır -->
            <div class="bg-gray-100 flex items-center text-gray-600 text-sm rounded-xl shadow h-42 px-4">
                <div class="grid grid-cols-3 gap-4 w-full">
                    <!-- Görsel -->
                    <div class="h-full flex items-center justify-center">
                        <img src="@/assets/Rectangle 21.png" alt="Side Image"
                            class="h-24 w-24 object-cover rounded-lg" />
                    </div>

                    <!-- Yazılar -->
                    <div class="col-span-2 flex flex-col justify-center overflow-hidden">
                        <!-- Başlık (tamamı gözüksün) -->
                        <h1 class="font-semibold text-base leading-snug mb-1">
                            More Airports to Use Greener ‘Glide’ Approach to Landing
                        </h1>

                        <!-- Yazar ve Tarih -->
                        <div class="flex gap-4 text-xs text-gray-500 mb-1">
                            <p>Yazar Adı</p>
                            <p>Tarih</p>
                        </div>

                        <!-- Açıklama (maks 3 satır, sonuna …) -->
                        <p class="text-xs text-gray-700 leading-tight line-clamp-3">
                            The Stopping Home Office Work’s Unproductive Problems (SHOW UP, get it?) Act of 2023 passed
                            the Republican-majority US House of Representatives on a close-to-party-line vote, sparking
                            a
                            debate on work productivity, remote flexibility and legislative priorities in modern
                            governance.
                        </p>

                        <!-- Devamını Oku -->
                        <button class="text-blue-600 hover:underline text-xs self-start">
                            Devamını Oku
                        </button>
                    </div>
                </div>


            </div>

        </div>
    </div>
</template>