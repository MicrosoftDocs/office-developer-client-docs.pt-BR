---
title: Método Append (Grupos do ADOX)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be31cc01122aa24eff2acb8396be2caab33c7dd4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863056"
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
> [!OBSERVAçãO] Antes de um objeto **Group** ser anexado à coleção **Groups** de um objeto **User**, na coleção **Groups** do [Catálogo](name-property-adox.md) já deve existir um objeto **Group** com o mesmo **Nome** daquele a ser anexado.


