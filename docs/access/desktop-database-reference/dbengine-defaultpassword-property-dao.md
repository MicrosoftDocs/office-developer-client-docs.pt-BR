---
title: Propriedade DBEngine.DefaultPassword (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5b1195b4217ca72374402b361b09d540583bf06
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465291"
---
# <a name="dbenginedefaultpassword-property-dao"></a>Propriedade DBEngine.DefaultPassword (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define a senha utilizada para criar o **Workspace** padrão quando ele é inicializado. **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . DefaultPassword

*expressão* Uma variável que representa um objeto **DBEngine** .

## <a name="remarks"></a>Comentários

A configuração para **DefaultPassword** é um tipo de dados de cadeia de caracteres que pode conter até 20 caracteres. Ele pode conter qualquer caractere exceto ASCII 0.


> [!NOTE]
> <P>[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</P>



Por padrão, a propriedade **DefaultUser** é definida como "admin" e a propriedade **DefaultPassword** é definida como uma sequência de comprimento zero ("").

Normalmente, use o método **CreateWorkspace** para criar um objeto **Workspace** com um determinado nome de usuário e senha. Entretanto, para compatibilidade com versões anteriores e para sua conveniência, quando você não implementa um banco de dados seguro, o mecanismo de banco de dados do Microsoft Access cria automaticamente um objeto **Workspace** padrão se um ainda não foi aberto. Nesse caso, os valores das propriedades **DefaultUser** e **DefaultPassword** definem o usuário e a senha para o objeto **Workspace** padrão.

Para essa propriedade ser efetivada, você deve defini-la antes de chamar quaisquer métodos DAO.
