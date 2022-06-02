# Modal

Learn how to create a Modal using Styled Components

1. Ceate Modal Container Component

```javascript
import styled from 'styled-components';

const ModalContainer = styled.div`
  align-items: center;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  flex-wrap: nowrap;
  height: 100%;
  left: 0;
  justify-content: center;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1000;
`;

export default ModalContainer;
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

3. Create Modal Component
```javascript
import { Fragment } from 'react';
import { createPortal } from 'react-dom';
import ModalContainer from './container';
import ModalContent from './content';

const Modal = ({ width }) => {
  return (
    <Fragment>
      {createPortal(
        <ModalContainer>
          <ModalContent width={width}>
            <h3>Modal Heading</h3>
            <p>Model Description</p>
          </ModalContent>
        </ModalContainer>,
        document.getElementById('root')
      )}
    </Fragment>
  );
};

export default Modal;
```
