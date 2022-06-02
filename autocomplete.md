
# Autocomplete

Learn how to create a Autocomplete using Styled Components

1. Create Input Component

```javascript
import styled from 'styled-components';

const Input = styled.input`
  appearance: none;
  background-color: rgba(255, 255, 255, 1);
  border: 1px solid rgba(210, 210, 210, 1);
  cursor: text;
  display: block;
  max-width: 100%;
  padding: 10px 15px;
  width: ${(props) => props.width};
`;

export default Input;
```
