---
title: Método getPermissions (ADOX)
TOCTitle: GetPermissions method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa5dda3c8e2ee8251fc54f4ff3bc12be0aca5002
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292241"
---
# <a name="getpermissions-method-adox"></a>Método getPermissions (ADOX)

**Aplica-se ao:** Access 2013, Office 2013

Retorna as permissões de um grupo ou usuário em um objeto ou contêiner de objetos.

## <a name="syntax"></a>Sintaxe

*ReturnValue* = *GroupOrUser*. GetPermissions (*Name*, *objecttype* \[,**\]objecttypeid)

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Long** que especifica um bitmask que contém as permissões do grupo ou usuário no objeto. Este valor pode ser uma ou mais das constantes [RightsEnum](rightsenum.md).

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Nome* |Um valor **Variant** que especifica o nome do objeto cujas permissões devem ser definidas. Defina *Name* como um valor nulo se desejar obter as permissões do contêiner de objetos.|
|*ObjectType* |Um valor **Long**, que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto para o qual devem ser obtidas permissões.|
|*ObjectTypeid* |Opcional. Um valor **Variant** que especifica o GUID de um tipo de objeto do provedor, não definido pela especificação do OLE DB. Este parâmetro será necessário se *ObjectType* for definido como **adPermObjProviderSpecific**; caso contrário, ele não será usado.|

