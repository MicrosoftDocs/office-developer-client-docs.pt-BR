---
title: Propriedade DBEngine.DefaultUser (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 15fc13b27b30c87bd3993b12303cc59b8a0115bf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462878"
---
# <a name="dbenginedefaultuser-property-dao"></a>Propriedade DBEngine.DefaultUser (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define o nome de usuário utilizado para criar o **Workspace** padrão quando ele é inicializado. **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . DefaultUser

*expressão* Uma expressão que retorna um objeto **DBEngine** .

## <a name="remarks"></a>Comentários

A configuração para **DefaultUser** é um tipo de dados de cadeia de caracteres. Ele pode ser de 1 a 20 caracteres longos no Microsoft Access e espaços de trabalho podem incluir caracteres alfabéticos, caracteres acentuados, números, espaços e símbolos, exceto para: "(aspas), / (barra), \\ (barra invertida), \[ \] (colchetes) ,: (dois-pontos), | (pipe), \< (menos-sinal), \> (maior-sinal), + (sinal de adição,) = (sinal de igual), (ponto e vírgula), (vírgula)? (ponto de interrogação), \* (asterisco), levando espaços e caracteres de controle (ASCII 00 a ASCII 31).


> [!NOTE]
> <P>[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</P>



Por padrão, a propriedade **DefaultUser** é definida como "admin" e a propriedade **DefaultPassword** é definida como uma sequência de comprimento zero ("").

Os nomes de usuários normalmente não fazem distinção entre maiúsculas e minúsculas; contudo, se você estiver recriando uma conta de usuário que tenha sido excluída ou criada em um grupo de trabalho diferente, o nome do usuário deverá corresponder exatamente ao nome original, inclusive em relação à maiúsculas e minúsculas. As senhas fazem distinção entre maiúsculas e minúsculas.

Normalmente, use o método **CreateWorkspace** para criar um objeto **Workspace** com um determinado nome de usuário e senha. Entretanto, para compatibilidade com versões anteriores e para sua conveniência, quando você não implementa um banco de dados seguro, o mecanismo de banco de dados do Microsoft Access cria automaticamente um objeto **Workspace** padrão se um ainda não foi aberto. Nesse caso, os valores das propriedades **DefaultUser** e **DefaultPassword** definem o usuário e a senha para o objeto **Workspace** padrão.

Para essa propriedade ser efetivada, você deve defini-la antes de chamar quaisquer métodos DAO.
