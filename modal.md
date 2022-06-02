# Modal

Learn how to create a Modal using Styled Components

1. Ceate Modal Dialog Component

```javascript
import styled from 'styled-components';

const ModalDialog = styled.div`
  align-items: center;
  display: flex;
  flex-wrap: nowrap;
  height: 100%;
  left: 0;
  justify-content: center;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1002;
`;

export default ModalDialog;
```

2. Ceate Modal Content Component

```javascript
import styled from 'styled-components';

const ModalContent = styled.div`
  background-color: #fff;
  margin: auto;
  max-width: 100%;
  padding: 20px 15px;
  width: ${(props) => props.width};
`;

export default ModalContent;
```
