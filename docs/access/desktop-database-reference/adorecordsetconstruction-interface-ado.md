---
title: Interface ADORecordsetConstruction (ADO)
TOCTitle: ADORecordsetConstruction Interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0b99fcfe4fadc3dddf5937ba1043875de43e88d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464276"
---
# <a name="adorecordsetconstruction-interface-ado"></a>Interface ADORecordsetConstruction (ADO)


**Aplica-se a**: Access 2013 | Office 2013

A interface **ADORecordsetConstruction** é utilizada para construir um objeto **Recordset** do ADO a partir de um objeto **Rowset** do banco de dados OLE em um aplicativo C/C++.

Essa interface suporta as seguintes propriedades:

## <a name="properties"></a>Propriedades

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="chapter-property-ado.md">Capítulo</a></p></td>
<td><p>Leitura/gravação.<br />
Obtém/define um objeto de banco de dados OLE <strong>capítulo</strong> de/neste objeto <strong>Recordset</strong> do ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Leitura/gravação.<br />
Obtém/define um objeto <strong>RowPosition</strong> do OLE DB a partir de/neste objeto <strong>Recordset</strong> do ADO.</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Conjunto de linhas</a></p></td>
<td><p>Leitura/gravação.<br />
Obtém/define um objeto <strong>Rowset</strong> do OLE DB a partir de/neste objeto <strong>Recordset</strong> do ADO.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Métodos

Nenhum.

## <a name="events"></a>Eventos

Nenhum.

## <a name="remarks"></a>Comentários

Dado um objeto **Rowset** do OLE DB (pRowset), a construção de um objeto do **Recordset** do ADO (), a construção de um **Recordset** do ADO as quantidades de objeto (adoRs) às três operações básicas a seguir:

1. Criar um objeto **Recordset** do ADO:
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. Consultar a interface **IADORecordsetConstruction** no objeto **Recordset**:

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. Chamar o IADORecordsetConstruction::put\_Rowset o método de propriedade para definir o objeto Rowset do OLE DB no objeto Recordset do ADO:

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
O objeto resultante agora representa o objeto **Recordset** do ADO construído a partir do objeto **Rowset** do OLE DB.

Também é possível construir um objeto **Recordset** do ADO a partir de um objeto **Chapter** ou **RowPosition** do banco de dados OLE.

## <a name="requirements"></a>Requisitos

- **Versão:** ADO 2.0 e posterior

- **Biblioteca:** msado15.dll

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

