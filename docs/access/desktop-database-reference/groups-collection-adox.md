---
title: Coleção Groups (ADOX)
TOCTitle: Groups Collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 099b9b4034d64f768513cfa5c9a28b89bef89ef8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880989"
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
> <P>[!OBSERVAçãO] Antes de um objeto <STRONG>Group</STRONG> ser anexado à coleção <STRONG>Groups</STRONG> de um objeto <STRONG>User</STRONG>, na coleção <STRONG>Groups</STRONG> do <A href="name-property-adox.md">Catálogo</A> já deve existir um objeto <STRONG>Group</STRONG> com o mesmo <STRONG>Nome</STRONG> daquele a ser anexado.</P>


