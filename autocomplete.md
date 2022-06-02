
# Autocomplete

Learn how to create a Autocomplete using Styled Components

1. Create Input Component

```javascript
import styled from 'styled-components';

const Input = styled.input`
  border: 1px solid #d6d6d6;
  display: block;
  max-width: 100%;
  padding: 10px 15px;
  width: ${(props) => props.width};
`;

export default Input;
```
