# Angular-Rating
This repo is related to the rating

# Table of Contents
Installation
Usage
Options
Themes
Issues
Author

# Installation
Install it with npm

`npm install ang-rating `

# Basic usage:
Import  AngRatingModule` in the root module

` import { AngRatingModule } from "ang-rating" `

`@NgModule({
  imports: [
    // ...
    AngRatingModule
  ]
})`

In your template

`<ang-rating [(ngModel)]="ratingThumsUp.value" [title]="ratingThumsUp.title"
[color]="ratingThumsUp.color" [type]="ratingThumsUp.type" [max]="ratingThumsUp.max" (rateChange)="onThumsUp($event)"
[min]="ratingThumsUp.min" [step]="ratingThumsUp.step" [input]="ratingThumsUp.input"></ang-rating> `


# Rating options (inputs):
*[ngModel]*: Current rating. It is required.

*[type]*: Type of rating that can be dropdown,number and any Mat Icon name ex. thumb_up or thumb_down, default star

*[max]*: Maximal rating that can be given using this widget, default 5.

*[min]*: Minimum rating that can be given using this widget, default 1.

*[input]*: Allow user to give rating(editable) otherwise it will be read only. default false.

*[theme]*: Theme class.theme number-block for number rating and icon-block for icon.theme is not require for dropdown rating.

*[step]*: step class.step that can be range of min and max.

*[title]*: Titles array. array length should be equal to the max value, each index represents the rating title, default [].

*[format]*: A format indicating if format is 'percentage' then rating value is in percentage, default is value.

*(rateChange)*: An event fired when a user selects a new rating.


*Number rating example*

`<ang-rating [(ngModel)]="ratingThumsUp.value" [title]="ratingThumsUp.title"
[color]="ratingThumsUp.color" [type]="ratingThumsUp.type" [max]="ratingThumsUp.max" (rateChange)="onThumsUp($event)"
[min]="ratingThumsUp.min" [step]="ratingThumsUp.step" [input]="ratingThumsUp.input"></ang-rating>`

It can be used with typescript file pass the value to rating direcive, for example:

   'this.ratingThumsUp = {
        type: 'star',
        value: 30,
        min: 10,
        max: 100,
        step: 10,
        input: true,
        color: ['#ff0000', '#ffa500', '#ffd280', '#008000']
    };'

