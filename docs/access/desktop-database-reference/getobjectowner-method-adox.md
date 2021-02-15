---
title: Método GetObjectOwner (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 948464534f9bbfbea50c8eba2c926dea9cb9bcac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292255"
---
# <a name="getobjectowner-method-adox"></a>Método GetObjectOwner (ADOX)

**Aplica-se ao:** Access 2013, Office 2013

Retorna o proprietário de um objeto em um [Catálogo](catalog-object-adox.md).

## <a name="syntax"></a>Sintaxe

*Proprietário*  =  *Catálogo*. GetObjectOwner(*ObjectName*, *ObjectType* \[ ,*ObjectTypeId* \] )

## <a name="return-value"></a>Valor de retorno

Retorna um valor **String** que especifica o [Nome](name-property-adox.md) do [Usuário](user-object-adox.md) ou [Grupo](group-object-adox.md) proprietário do objeto.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*ObjectName* |Um valor **String** que especifica o nome do objeto para o qual o usuário deve ser retornado.|
|*ObjectType* |Um valor **Long** que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto cujo proprietário deve ser obtido.|
|*ObjectTypeId* |Opcional. Um valor **Variant** que especifica o GUID de um tipo de objeto do provedor, não definido pela especificação do OLE DB. Este parâmetro será necessário se *ObjectType* for definido como **adPermObjProviderSpecific**; caso contrário, ele não será usado.|

## <a name="remarks"></a>Comentários

Ocorrerá um erro se o provedor não oferecer suporte para o retorno de proprietários de objetos.

