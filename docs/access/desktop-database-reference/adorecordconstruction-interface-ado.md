---
title: Interface ADORecordConstruction (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a53eb107bab0d31606dc161b9f9c910894c5bc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281623"
---
# <a name="adorecordconstruction-interface-ado"></a>Interface ADORecordConstruction (ADO)


**Aplica-se ao:** Access 2013, Office 2013

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

Define o contêiner de um objeto <strong>Row</strong> do banco de dados OLE nesse objeto <strong>Record</strong> do ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Linha</a></p></td>
<td><p>Leitura/gravação.<br />

Obtém/define um objeto <strong>Row</strong> do banco de dados OLE desse/nesse objeto <strong>Record</strong> do ADO.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Métodos

Nenhum.

## <a name="events"></a>Eventos

Nenhum.

## <a name="remarks"></a>Comentários

Dado um objeto de **linha** OLE DB (Prow), a construção de um objeto **Record** do ADO (), a construção de um objeto **Record** do ADO (adoR), valores para as três operações básicas a seguir:

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

3.  Chame o método de propriedade de **linha IADORecordConstruction::p\_UT** para definir o objeto de **linha** OLE DB no objeto **Record** do ADO:
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
O objeto **adoR** resultante agora representa o objeto **Record** do ADO construído a partir do objeto **Row** do banco de dados OLE.

Um objeto **Record** do ADO também pode ser construído a partir do contêiner de um objeto **Row** do banco de dados OLE.

## <a name="requirements"></a>Requirements

**Versão:** ADO 2.0 e posterior

**Biblioteca:** msado15.dll

**UUID:** 00000567-0000-0010-8000-00AA006D2EA4

