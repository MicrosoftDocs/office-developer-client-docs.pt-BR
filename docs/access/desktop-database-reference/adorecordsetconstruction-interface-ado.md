---
title: Interface ADORecordsetConstruction (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98342d5456c545e6da8539c11f616c08fd52a932
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281630"
---
# <a name="adorecordsetconstruction-interface-ado"></a>Interface ADORecordsetConstruction (ADO)


**Aplica-se ao:** Access 2013, Office 2013

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

Obtém/define um objeto <strong>Chapter</strong> do banco de dados OLE desse/nesse objeto <strong>Recordset</strong> do ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Leitura/gravação.<br />

Obtém/define um objeto <strong>RowPosition</strong> do banco de dados OLE desse/nesse objeto <strong>Recordset</strong> do ADO.</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Rowset</a></p></td>
<td><p>Leitura/gravação.<br />

Obtém/define um objeto <strong>Rowset</strong> do banco de dados OLE desse/nesse objeto <strong>Recordset</strong> do ADO.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Métodos

Nenhum.

## <a name="events"></a>Eventos

Nenhum.

## <a name="remarks"></a>Comentários

Dado um objeto **Rowset** do OLE DB (pRowset ), a construção de um objeto **Recordset** do ADO (), a construção de um objeto **Recordset** do ADO (adoRs ) equivale às três operações básicas a seguir:

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

3. Chame o método da propriedade IADORecordsetConstruction::p ut Rowset para definir o objeto Rowset OLE DB no objeto \_ Recordset do ADO:

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
O objeto resultante agora representa o objeto **Recordset do** ADO construído a partir do objeto **Rowset** do OLE DB.

Também é possível construir um objeto **Recordset** do ADO a partir de um objeto **Chapter** ou **RowPosition** do banco de dados OLE.

## <a name="requirements"></a>Requisitos

- **Versão:** ADO 2.0 e posterior

- **Biblioteca:** msado15.dll

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

