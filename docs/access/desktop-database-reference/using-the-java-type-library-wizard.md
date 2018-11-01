---
title: Usando o Java Type Library Wizard
TOCTitle: Using the Java Type Library Wizard
ms:assetid: 96af770c-c7c2-c905-3c3e-383a5b99cab2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249670(v=office.15)
ms:contentKeyID: 48546455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 233e1a9e6237500b3d13e3234e7c6ddf4d556abc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884132"
---
# <a name="using-the-java-type-library-wizard"></a>Usando o Java Type Library Wizard


**Aplica-se a**: Access 2013, o Office 2013

O Java Type Library Wizard é um recurso do Visual J++ 1.x, integrado ao menu **Ferramentas** do ambiente de desenvolvimento. Sua função é pesquisar uma biblioteca de tipos e criar uma interface Java que permita acessar objetos COM. No Visual J++ 6.0, esse recurso foi substituído pelo [ADO for Windows Foundation Classes](ado-wfc-programming.md).

O Java Type Library Wizard produz resultados semelhantes aos das ferramentas de linha de comando incluídas com o [Microsoft SDK for Java](using-the-microsoft-sdk-for-java.md). Entretanto, você não pode depurar os invólucros de classe gerados pelo assistente, ao contrário dos invólucros de classe gerados pelo Microsoft SDK for Java.

O Java Type Library Wizard gera as classes no seguinte local: \\ \<diretório windows\>\\Java\\trustlib\\msado15. O arquivo Summary.txt, localizado no diretório que gerou as classes, mostra as definições de classe geradas por ele.

O Java Type Library Wizard converte os tipos enumerados, encontrados em qualquer biblioteca de tipos específica, no tipo INT (inteiro). Ele também define uma interface que corresponde a cada tipo enumerado na biblioteca de tipos. Você pode fazer referência aos valores de um tipo ADO enumerado usando esta sintaxe:

```vb 
 
msado15.<Enum Name>.<constant Name> 
```

Um exemplo disso é mostrado no fragmento de código a seguir para definição da propriedade **CommandType** de um objeto **Command**:

```vb 
 
Cmd1.putCommandType( msado15.CommandTypeEnum.adCmdStoredProc ); 
```

Também seria possível herdar do invólucro de tipo enumerado gerado pelo Java Type Library Wizard. Nesse caso, você poderia remover "msado15." da sintaxe. Entretanto, sua classe precisaria herdar de cada objeto Java e interface de tipo enumerado à qual ela se refere para tornar totalmente desnecessária a referência de msado15.\* na frente de todos os objetos ADO e valores enumerados.

Para obter mais informações sobre código de exemplo, consulte [Invólucros de classe ADO Java](ado-java-class-wrappers.md).

**Para executar o Java Type Library Wizard a partir Visual J++ versão 1.*x***

1.  No menu **Ferramentas**, selecione **Java Type Library Wizard**.

2.  Selecione "Biblioteca Microsoft ActiveX Data Objects" e clique em **OK**. Isso agora (re) gera arquivos no \\trustlib diretório para o ADO (por padrão em c:\\winnt\\java\\trustlib\\msado15). Se você tiver usado o Microsoft SDK for Java para já gerar classes para o ADO, elas serão substituídas por essas classes do Java Type Library Wizard.

3.  Para usar esses arquivos, abra seu projeto no Visual J++. No menu **Projeto**, escolha **Adicionar ao Projeto**. Selecione os **arquivos**e adicione todos os. Arquivos JAVA gerados no \\trustlib diretório (por padrão em c:\\winnt\\java\\trustlib\\msado15) ao seu projeto.

