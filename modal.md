# Modal

Learn how to create a Modal using Styled Components

<a href="https://codesandbox.io/s/modal-bcckh4" title="CodeSandbox Link">CodeSandbox Link</a>

1. Create Modal Container Component

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

2. Create Modal Content Component

```javascript
import styled from 'styled-components';

const ModalContent = styled.div`
  background-color: rgba(255, 255, 255, 1);
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

const Modal = ({ children, width }) => {
  return (
    <Fragment>
      {createPortal(
        <ModalContainer>
          <ModalContent width={width}>{children}</ModalContent>
        </ModalContainer>,
        document.getElementById('root')
      )}
    </Fragment>
  );
};

export default Modal;
```
