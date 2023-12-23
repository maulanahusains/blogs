<template>
    <table class="w-full">
        <thead class="text-left border border-transparent border-b-black">
            <tr>
                <slot name="thead">
                    <th>#</th>    
                    <th>Name</th>    
                    <th>Username</th>    
                </slot>
            </tr>
        </thead>
        <tbody class="text-left">
            <slot name="tbody">
                <tr>
                    <th>1</th>
                    <td>Maul</td>
                    <td>MaulHusain</td>
                </tr>
            </slot>
        </tbody>
    </table>
</template>