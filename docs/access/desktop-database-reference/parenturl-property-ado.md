---
title: Propriedade ParentURL (ADO)
TOCTitle: ParentURL property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e3735147f813d904c206910ff319913f056946e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287714"
---
# <a name="parenturl-property-ado"></a>Propriedade ParentURL (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Indica uma sequência de URL absoluta que aponta para o [Record](record-object-ado.md) pai do objeto **Record** atual.

## <a name="return-value"></a>Valor de retorno

Retorna um valor **String** que indica a URL do **Record** pai.

## <a name="remarks"></a>Comentários

A propriedade **ParentURL** depende da origem utilizada para abrir o objeto **Record**. Por exemplo, o **Record** pode ser aberto com uma origem contendo um nome de caminho relativo de um diretório referido pela propriedade [ActiveConnection](activeconnection-property-ado.md).

Suponha que "second" seja uma pasta contida em "first". Abra o objeto **Record** da seguinte maneira:

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

Agora, o valor da **propriedade ParentURL** é **a propriedade ParentURL** é " , o mesmo que https://first **ActiveConnection**.

A fonte também pode ser uma URL absoluta, como " https://first/second . A **propriedade ParentURL** é então " https://first , o nível acima . A **propriedade ParentURL** é então " https://first " , o nível acima de "segundo" .

Essa propriedade poderá ser um valor nulo se:

- Não houver pai para o objeto atual; por exemplo, se o objeto **Record** representar a raiz de um diretório.

- O objeto **Record** representar uma entidade que não possa ser especificada com uma URL.

Esta propriedade é somente leitura.


> [!NOTE]
> - [!OBSERVAçãO] Esta propriedade conta com suporte somente de provedores de origem de documento, como [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [Registros e campos fornecidos pelo provedor](records-and-provider-supplied-fields.md).
> - [!OBSERVAçãO] URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing. Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md). 
> - [!OBSERVAçãO] Se o registro atual contiver um registro de dados do **Recordset** de um ADO, acessar a propriedade **ParentURL** causará um erro de tempo de execução, indicando que nenhuma URL é possível.


