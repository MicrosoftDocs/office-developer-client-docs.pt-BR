---
title: Método GetPermissions (ADOX)
TOCTitle: GetPermissions Method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b7e6603d8da5bafc7a479cb8bfe94577a0679bd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464421"
---
# <a name="getpermissions-method-adox"></a>Método GetPermissions (ADOX)


**Aplica-se a**: Access 2013 | Office 2013


Retorna as permissões de um grupo ou usuário em um objeto ou contêiner de objetos.

## <a name="syntax"></a>Sintaxe

*ReturnValue* = *GrupoOuUsuário*. GetPermissions (*nome*, *ObjectType* \[,*ObjectTypeId*\])

## <a name="return-value"></a>Return Value

Retorna um valor **Long** que especifica um bitmask que contém as permissões do grupo ou usuário no objeto. Este valor pode ser uma ou mais das constantes [RightsEnum](rightsenum.md).

## <a name="parameters"></a>Parâmetros

  - *Name*

  - Um valor **Variant** que especifica o nome do objeto cujas permissões devem ser definidas. Definir o *nome* como um valor nulo se você deseja obter as permissões para o contêiner do objeto.

  - *ObjectType*

  - Um valor **Long**, que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto para o qual devem ser obtidas permissões.

  - *ObjectTypeId*

  - Opcional. Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB. Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.
