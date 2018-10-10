---
title: Interface ADORecordConstruction (ADO)
TOCTitle: ADORecordConstruction Interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44272067d8018836fd7eb3d6cfaa762780f69868
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463677"
---
# <a name="adorecordconstruction-interface-ado"></a>Interface ADORecordConstruction (ADO)


**Aplica-se a**: Access 2013 | Office 2013

A interface **ADORecordConstruction** é utilizada para construir um objeto **Record** do ADO a partir de um objeto **Row** do banco de dados OLE em um aplicativo C/C++.

Essa interface suporta as seguintes propriedades:

## <a name="properties"></a>Propriedades

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="parentrow-property-ado.md">ParentRow</a></p></td>
<td><p>Somente gravação.<br />
Define o contêiner de um objeto <strong>Row</strong> do OLE DB neste objeto <strong>Record</strong> do ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Row</a></p></td>
<td><p>Leitura/gravação.<br />
Obtém/define um objeto do OLE DB <strong>linha</strong> a partir de/neste objeto <strong>Record</strong> do ADO.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Métodos

Nenhum.

## <a name="events"></a>Eventos

Nenhum.

## <a name="remarks"></a>Comentários

Dado um objeto OLE DB **linha** (pRow), a construção de um objeto de **registro** do ADO (), a construção de um objeto **Record** do ADO (objeto adoR), quantidades às três operações básicas a seguir:

1.  Criar um objeto **Record** do ADO:
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  Consultar a interface **IADORecordConstruction** no objeto **Record**:
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  Chamar o **IADORecordConstruction::put\_linha** método de propriedade para definir o objeto OLE DB **linha** no objeto **Record** do ADO:
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
O objeto **adoR** resultante agora representa o objeto **Record** do ADO construído a partir do objeto **Row** do banco de dados OLE.

Um objeto **Record** do ADO também pode ser construído a partir do contêiner de um objeto **Row** do banco de dados OLE.

## <a name="requirements"></a>Requisitos

**Versão:** ADO 2.0 e posterior

**Biblioteca:** msado15.dll

**UUID:** 00000567-0000-0010-8000-00AA006D2EA4

