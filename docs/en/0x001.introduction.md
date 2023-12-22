# Introduction

Welcome to the world of robot development. Based on the SDK of AutoXing Robot, you can quickly realize the comprehensive control of the robot and create your own robot. This document describes how to develop a robot application using JavaScript.

## SDK Organizational Structure

### Basic Interfaces

The basic interfaces are fine-grained API calls that can be invoked in code at any time. The interface returns the result of the call with a Promise.

### Advanced Functions

Advanced functions provide API calls to cloud services, returning the call results through Promises in a unified manner.

### Functional Units

Functional components provide advanced robot operations, such as navigation and patrol, automatic recharge, etc.

## Preliminary Knowledge

SDK kits are provided in the form of Node.js modules. Developers are required to have some knowledge of Node.js and JavaScript. If you are not familiar with Node.js and JavaScript, please check the official Node.js and JavaScript documentation first:

* [Node.js official document](https://nodejs.org/zh-cn/docs/)
* [JavaScript document](https://developer.mozilla.org/en-US/docs/Web/JavaScript)