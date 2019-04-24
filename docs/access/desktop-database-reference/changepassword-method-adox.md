---
title: Método ChangePassword (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df67774b9b38b5fbcc836a2ea0dfc17886d67107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296525"
---
# <a name="changepassword-method-adox"></a>Método ChangePassword (ADOX)

**Aplica-se ao:** Access 2013, Office 2013

Altera a senha de uma conta de usuário.

## <a name="syntax"></a>Sintaxe

*User*. ChangePassword*SenhaAntiga*, *newPassword*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*SenhaAntiga* |Um valor **String** que especifica a senha existente do usuário. Se o usuário não tiver uma senha no momento, usar uma sequência vazia ("") para *OldPassword*.|
|*NewPassword* |Um valor **String** que especifica a nova senha.|

## <a name="remarks"></a>Comentários

Por motivos de segurança, a senha antiga deve ser especificada, além da nova senha.

Ocorrerá um erro se o provedor não oferecer suporte para a administração de propriedades de objetos de confiança.

