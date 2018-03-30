

```javascript
/**
*
* 这里的modalManager 可以考虑下我们在弹出层的所有组件
* alert, popup, modal , 等等
*/
MoalManager.open(<Modal />);

node;
modals = [];  // 队列
ModalManager = {
    open(Compoent) {
        modals.push(Component);
        if (modals.length === 1) {
            renderModal();
        }
    }
    close() {
        onClose && onClose(() => {
            ReactDom.unmountComponentAtNode(node);
            renderModal();
        })
    }
}

renderModal = () => {
    if (modals.length == 0)
        return
    const component = modals.shift();
    if (!node) {
        node = document.createElement('div');
        document.body.appendChild(node);
    }
    ReactDom.render(component,node);
}

// ------------------------------------------------
// ------------------------------------------------
// react-router-proxy-loader, react-proxy-loader, react-router-loader.

```

