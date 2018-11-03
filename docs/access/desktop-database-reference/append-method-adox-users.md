---
title: Método Append (Usuários do ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf855fc6e829ebfbe3809925bf1ab8ca337d3f96
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949408"
---
# <a name="append-method-adox-users"></a>Método Append (Usuários do ADOX)

**Aplica-se a**: Access 2013, o Office 2013

Adiciona um novo objeto [User](user-object-adox.md) à coleção [Users](users-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Os usuários*. Acrescentar*usuário*\[,*senha*\]

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*User* |Um valor **Variant** que contém o objeto **User** a ser anexado ou o nome do usuário a ser criado e anexado.|
|*Password* |Opcional. Um valor **String** que contém a senha do usuário. O parâmetro *Password* corresponde ao valor especificado pelo método [ChangePassword](changepassword-method-adox.md) de um objeto de **usuário** .|

## <a name="remarks"></a>Comentários

A coleção **Users** de um objeto [Catalog](catalog-object-adox.md) representa todos os usuários do catálogo. A coleção **Users** de um objeto [Group](group-object-adox.md) representa apenas os usuários associados ao grupo específico.

Ocorrerá um erro se o provedor não oferecer suporte para a criação de usuários.

> [!NOTE]
> [!OBSERVAçãO] Antes de um objeto **User** ser anexado à coleção **Users** de um objeto **Group**, na coleção **Users** do [Catálogo](name-property-adox.md) já deve existir um objeto **User** com o mesmo **Nome** daquele a ser anexado.


