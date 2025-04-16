# CL RUT Validator

A TypeScript package for validating and formatting Chilean RUT (Rol Único Tributario) numbers.

[![Version](https://img.shields.io/npm/v/cl-rut-validator?logo=npm)](https://www.npmjs.com/bennu/cl-rut-validator)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript)](https://www.typescriptlang.org/)
[![Downloads](https://img.shields.io/npm/dm/bennucl-rut-validator)](https://www.npmjs.com/bennu/cl-rut-validator)
[![Bundle Size](https://img.shields.io/bundlephobia/minzip/cl-rut-validator)](https://bundlephobia.com/bennu/cl-rut-validator)
[![Test Coverage](https://img.shields.io/badge/coverage-100%25-brightgreen)](https://github.com/bennu/cl-rut-validator)
[![License](https://img.shields.io/badge/license-MIT-blue.svg?logo=opensourceinitiative)](https://opensource.org/license/mit)

## 📋 Features

- **Zero Dependencies** - Lightweight and efficient implementation
- **TypeScript Native** - Full type definitions and type safety
- **Comprehensive Validation** - Complete validation for Chilean RUT numbers

## 🚀 Installation

```bash
# Using npm
npm install cl-rut-validator

# Using yarn
yarn add cl-rut-validator

# Using pnpm
pnpm add cl-rut-validator
```

## 💻 Usage

### JavaScript (CommonJS)

```javascript
const { isValidRut, validateRut, formatRut } = require('cl-rut-validator');

// Basic validation
console.log(isValidRut('12.345.678-5')); // true

// Detailed validation
const validation = validateRut('12.345.678-5');
console.log(validation);
/*
{
  isValid: true,
  formatted: '12.345.678-5',
  raw: '123456785',
  rutNumber: '12345678',
  verificationDigit: '5'
}
*/

// Formatting
console.log(formatRut('123456785')); // '12.345.678-5'
```

### TypeScript / ES Modules

```typescript
import { isValidRut, validateRut, formatRut, RutValidationResult } from 'cl-rut-validator';

// Basic validation
console.log(isValidRut('12.345.678-5')); // true

// Detailed validation with type safety
const validation: RutValidationResult = validateRut('12.345.678-5');
console.log(validation);
/*
{
  isValid: true,
  formatted: '12.345.678-5',
  raw: '123456785',
  rutNumber: '12345678',
  verificationDigit: '5'
}
*/

// Formatting
console.log(formatRut('123456785')); // '12.345.678-5'
```

## 🔍 Understanding Chilean RUT

The Chilean RUT (Rol Único Tributario) is the national tax ID number in Chile. It consists of:

1. A sequence of digits (typically 7-8 digits)
2. A verification digit (0-9 or 'K')

The verification digit is calculated using Module 11 algorithm to ensure validity.

## 🔒 Security Features

This package includes several security measures:

- Protection against DoS attacks with input length limits
- Proper type handling for all inputs

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.