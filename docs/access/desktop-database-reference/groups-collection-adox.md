---
title: Coleção Groups (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 21f1880a9effca6e51bc1e8b52a58dce22ce1ea9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712516"
---
# <a name="groups-collection-adox"></a>Coleção Groups (ADOX)

**Aplica-se a**: Access 2013, o Office 2013

Contém todos os objetos [Group](group-object-adox.md) de um catálogo ou usuário.

## <a name="remarks"></a>Comentários

A coleção **Groups** de um [Catálogo](catalog-object-adox.md) representa todas as contas de grupo do catálogo. A coleção **Groups** de um [Usuário](user-object-adox.md) representa apenas o grupo ao qual o usuário pertence.

O método [Append](append-method-adox-groups.md) de uma coleção **Groups** é exclusivo de ADOX. Você pode:

- Adicionar um novo grupo de segurança à coleção com o método **Append**.

As propriedades e métodos restantes são padrão das coleções do ADO. Você pode:

- Acessar um grupo na coleção com a propriedade [Item](item-property-ado.md).

- Retornar o número de grupos contidos na coleção com a propriedade [Count](count-property-ado.md).

- Remover um grupo da coleção com o método [Delete](delete-method-adox-collections.md).

- Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).

> [!NOTE]
> [!OBSERVAçãO] Antes de um objeto **Group** ser anexado à coleção **Groups** de um objeto **User**, na coleção **Groups** do [Catálogo](name-property-adox.md) já deve existir um objeto **Group** com o mesmo **Nome** daquele a ser anexado.


