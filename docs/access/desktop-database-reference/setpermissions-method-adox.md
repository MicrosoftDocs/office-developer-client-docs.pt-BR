---
title: Método setPermissions (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f9b393e90d579c131865b112263efd0aef3216b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314578"
---
# <a name="setpermissions-method-adox"></a>Método setPermissions (ADOX)

**Aplica-se ao:** Access 2013, Office 2013

Especifica as permissões referentes a um grupo ou usuário em um objeto.

## <a name="syntax"></a>Sintaxe

*GroupOrUser*. SetPermissions*Name*, *objecttype*, *Action*, *Rights* \[,*Inherit* \] \[, objecttypeid**\]

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Name* |Um valor **String** que especifica o nome do objeto para o qual permissões serão definidas.|
|*ObjectType* |Um valor **Long** que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto para o qual permissões serão obtidas.|
|*Action* |Um valor **Long** que pode ser uma das constantes [ActionEnum](actionenum.md) que especifica o tipo de ação a ser executada durante a definição de permissões.|
|*Rights* |Um valor **Long** que pode ser uma máscara de bits de uma ou mais constantes [RightsEnum](rightsenum.md), que indica os direitos a serem definidos.|
|*Inherit* |Opcional. Um valor **Long** que pode ser uma das constantes [InheritTypeEnum](inherittypeenum.md), que especifica como os objetos herdarão essas permissões. O valor padrão é **adInheritNone**.|
|*ObjectTypeid* |Opcional. Um valor **Variant** que especifica o GUID de um tipo de objeto do provedor, não definido pela especificação do OLE DB. Este parâmetro será necessário se *ObjectType* for definido como **adPermObjProviderSpecific**; caso contrário, ele não será usado.|

## <a name="remarks"></a>Comentários

Ocorrerá um erro se o provedor não oferecer suporte à definição de direitos de acesso para grupos ou usuários.

> [!NOTE]
> Durante a chamada de **SetPermissions**, a definição de Actions como **adAccessRevoke** substituirá as configurações do parâmetro *Rights*. Não defina *Actions* como **adAccessRevoke** se desejar que os direitos especificados no parâmetro *Rights* entrem em vigor.


