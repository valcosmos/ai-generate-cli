# Table/index.ts

```typescript
export { default as Table } from './Table';
export type { TableProps } from './interface';
```

# Table/interface.ts

```typescript
interface TableProps {
    data: {
        name: string,
        age: number,
        email: string,
    }[]
}

export type { TableProps };
```

# Table/Table.tsx

```tsx
import { Table as AntTable } from 'antd';
import { TableProps } from './interface';
import './styles.scss';

const Table = ({ data }: TableProps) => {
    const columns = [
        {
            title: '姓名',
            dataIndex: 'name',
            key: 'name',
        },
        {
            title: '年龄',
            dataIndex: 'age',
            key: 'age',
        },
        {
            title: '邮箱',
            dataIndex: 'email',
            key: 'email',
        },
    ];
  
    return <AntTable columns={columns} dataSource={data} />;
};

export default Table;
```

# Table/styles.scss

```scss
ant-table {
  // 样式内容，按需添加
}
```