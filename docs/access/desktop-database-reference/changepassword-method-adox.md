---
title: Método ChangePassword (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f11cfaddc99a0e10a86e0df9a7a187c4e89fc794
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921058"
---
# <a name="changepassword-method-adox"></a>Método ChangePassword (ADOX)


**Aplica-se a**: Access 2013, o Office 2013



Altera a senha de uma conta de usuário.

## <a name="syntax"></a>Sintaxe

O *usuário*. ChangePassword*senhaantiga*, *NewPassword*

## <a name="parameters"></a>Parâmetros

  - *Senhaantiga*

  - Um valor **String** que especifica a senha existente do usuário. Se o usuário não tiver uma senha no momento, usar uma sequência vazia ("") para *OldPassword*.

  - *NewPassword*

  - Um valor **String** que especifica a nova senha.

## <a name="remarks"></a>Comentários

Por motivos de segurança, a senha antiga deve ser especificada, além da nova senha.

Ocorrerá um erro se o provedor não oferecer suporte para a administração de propriedades de objetos de confiança.

