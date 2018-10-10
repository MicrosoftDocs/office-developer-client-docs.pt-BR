---
title: Método Append (Grupos do ADOX)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76c602896a629881d06a3f3cf80326e02340186e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465011"
---
# <a name="append-method-adox-groups"></a>Método Append (Grupos do ADOX)


**Aplica-se a**: Access 2013 | Office 2013



Adiciona um novo objeto [Group](group-object-adox.md) à coleção [Groups](groups-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Grupos*. Acrescentar um*grupo*

## <a name="parameters"></a>Parâmetros

  - *Group*

  - O objeto **Group** a ser anexado ou o nome do grupo a ser criado e anexado.

## <a name="remarks"></a>Comentários

A coleção **Groups** de um [Catálogo](catalog-object-adox.md) representa todas as contas de grupo do catálogo. A coleção **Groups** de um [Usuário](user-object-adox.md) representa apenas o grupo ao qual o usuário pertence.

Ocorrerá um erro se o provedor não oferecer suporte para a criação de grupos.


> [!NOTE]
> <P>[!OBSERVAçãO] Antes de um objeto <STRONG>Group</STRONG> ser anexado à coleção <STRONG>Groups</STRONG> de um objeto <STRONG>User</STRONG>, na coleção <STRONG>Groups</STRONG> do <A href="name-property-adox.md">Catálogo</A> já deve existir um objeto <STRONG>Group</STRONG> com o mesmo <STRONG>Nome</STRONG> daquele a ser anexado.</P>


