---
title: Método SetPermissions (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9ea1c08223282654af636326ba9a8c2bfe70e67
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949597"
---
# <a name="setpermissions-method-adox"></a>Método SetPermissions (ADOX)

**Aplica-se a**: Access 2013, o Office 2013

Especifica as permissões referentes a um grupo ou usuário em um objeto.

## <a name="syntax"></a>Sintaxe

*GrupoOuUsuário*. SetPermissions*nome*, *ObjectType*, *ação*, *direitos* \[,*herdam* \] \[,*ObjectTypeId*\]

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Nome* |Um valor **String** que especifica o nome do objeto para o qual permissões serão definidas.|
|*ObjectType* |Um valor **Long** que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto para o qual permissões serão obtidas.|
|*Action* |Um valor **Long** que pode ser uma das constantes [ActionEnum](actionenum.md) que especifica o tipo de ação a ser executada durante a definição de permissões.|
|*Rights* |Um valor **Long** que pode ser uma máscara de bits de uma ou mais constantes [RightsEnum](rightsenum.md), que indica os direitos a serem definidos.|
|*Inherit* |Opcional. Um valor **Long** que pode ser uma das constantes [InheritTypeEnum](inherittypeenum.md), que especifica como os objetos herdarão essas permissões. O valor padrão é **adInheritNone**.|
|*ObjectTypeId* |Opcional. Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB. Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.|

## <a name="remarks"></a>Comentários

Ocorrerá um erro se o provedor não oferecer suporte à definição de direitos de acesso para grupos ou usuários.

> [!NOTE]
> Ao chamar **SetPermissions**, a configuração de ações como **adAccessRevoke** substitui as configurações do parâmetro *direitos* . Não defina *ações* para **adAccessRevoke** se quiser que os direitos especificados no parâmetro *direitos* entrem em vigor.


