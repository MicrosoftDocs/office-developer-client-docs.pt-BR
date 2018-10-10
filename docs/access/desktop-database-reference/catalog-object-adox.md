---
title: Objeto Catalog (ADOX)
TOCTitle: Catalog Object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04622cd636d73beaf3124cda2584299443467973
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462464"
---
# <a name="catalog-object-adox"></a>Objeto Catalog (ADOX)


**Aplica-se a**: Access 2013 | Office 2013

Contém coleções ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md) e [Procedures](procedures-collection-adox.md)) que descrevem o catálogo de esquemas de uma fonte de dados.

## <a name="remarks"></a>Comentários

Você pode modificar o objeto **Catalog** adicionando ou removendo objetos ou modificando objetos existentes. Alguns provedores podem não oferecer suporte para todos os objetos **Catalog** ou podem oferecer suporte apenas para a exibição de informações do esquema.

Com as propriedades e métodos de um objeto **Catalog**, você pode:

  - Abrir o catálogo definindo a propriedade [ActiveConnection](activeconnection-property-adox.md) para um objeto [Connection](connection-object-ado.md) do ADO ou para uma sequência de conexão válida.

  - Criar um novo catálogo com o método [Create](create-method-adox.md).

  - Determinar os proprietários dos objetos em um **Catálogo** com os métodos [GetObjectOwner](getobjectowner-method-adox.md) e [SetObjectOwner](https://msdn.microsoft.com/library/jj249006\(v=office.15\)).

