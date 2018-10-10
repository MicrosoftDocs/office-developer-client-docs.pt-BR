---
title: Método GetObjectOwner (ADOX)
TOCTitle: GetObjectOwner Method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e20141e379cb207819744fd65b78abf7d2d15712
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465014"
---
# <a name="getobjectowner-method-adox"></a>Método GetObjectOwner (ADOX)


**Aplica-se a**: Access 2013 | Office 2013


Retorna o proprietário de um objeto em um [Catálogo](catalog-object-adox.md).

## <a name="syntax"></a>Sintaxe

*Proprietário* = *catálogo*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])

## <a name="return-value"></a>Return Value

Retorna um valor **String** que especifica o [Nome](name-property-adox.md) do [Usuário](user-object-adox.md) ou [Grupo](group-object-adox.md) proprietário do objeto.

## <a name="parameters"></a>Parâmetros

  - *ObjectName*

  - Um valor **String** que especifica o nome do objeto para o qual o usuário deve ser retornado.

  - *ObjectType*

  - Um valor **Long** que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto cujo proprietário deve ser obtido.

  - *ObjectTypeId*

  - Opcional. Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB. Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.

## <a name="remarks"></a>Comentários

Ocorrerá um erro se o provedor não oferecer suporte para o retorno de proprietários de objetos.

