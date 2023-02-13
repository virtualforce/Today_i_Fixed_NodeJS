# Generate Time Slots
A utility function for generating time slots between a given start time and end time with a given duration, excluding the unavailable slots.

## Tech Stack
This package uses JavaScript and TypeScript.


## Inputs

- startTime (required): The start time for generating the time slots.
- endTime (required): The end time for generating the time slots.
- duration (required): The duration of each time slot in minutes.
- unavailableSlots (optional): The unavailable time slots.

## Output

An array of time slots, each represented as an object with properties start and end, both of type string in ISO format.

## Throws
- Error: If the startTime is after the endTime.
- Error: If the duration is not a positive integer.


## Usage
You can use this function in your JavaScript or TypeScript project by importing or including it in your code.

Here is how you can use the function in your code:

```sh
import { generateTimeSlots } from './generateTimeSlots';

const startTime = '2022-01-01T09:00:00.000Z';
const endTime = '2022-01-01T17:00:00.000Z';
const duration = 30;
const unavailableSlots = [
  { start: '2022-01-01T10:00:00.000Z', end: '2022-01-01T11:00:00.000Z' },
  { start: '2022-01-01T13:00:00.000Z', end: '2022-01-01T14:00:00.000Z' },
];

const timeSlots = generateTimeSlots(startTime, endTime, duration, unavailableSlots);

console.log(timeSlots);

```

## Applications
This function can be useful in scheduling applications where you need to generate time slots between a given start and end time with a given duration, excluding the unavailable slots. For example, you can use it in a room booking system where you need to generate available time slots for a room.

This function can also be used in other applications that require time slot generation, such as appointment scheduling, task management, and resource allocation.