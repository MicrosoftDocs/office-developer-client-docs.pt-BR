---
title: Ação de macro LocalizarPróximoRegistro
TOCTitle: FindNextRecord Macro Action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 05dec445360d5c42636880982e27e0abd46d048e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883649"
---
# <a name="findnextrecord-macro-action"></a>Ação de macro LocalizarPróximoRegistro


**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **LocalizarPróximoRegistro** para localizar o próximo registro que atende aos critérios especificados pela ação **EncontrarRegistro** anterior ou o valor na caixa de diálogo **Localizar e Substituir** (na guia **Página Inicial**, clique em **Localizar**). Use a ação **LocalizarPróximoRegistro** para pesquisar registros várias vezes. Por exemplo, você pode se mover sucessivamente por todos os registros para buscar um cliente específico.

## <a name="setting"></a>Configuração

A ação **LocalizarPróximoRegistro** não tem nenhum argumento. A ação **LocalizarPróximoRegistro** localiza o próximo registro que atende aos critérios definidos pela ação **EncontrarRegistro** ou na caixa de diálogo **Localizar e Substituir**. Os argumentos da ação **EncontrarRegistro** são compartilhados com as opções na caixa de diálogo **Localizar e Substituir**.

Para definir os critérios de pesquisa, use a ação **EncontrarRegistro**. Normalmente, digita-se uma ação **EncontrarRegistro** em uma macro e usa-se a ação **LocalizarPróximoRegistro** para localizar registros sucessivos que atendem aos mesmos critérios. Para pesquisar registros somente quando um determinado critério é atendido, você pode digitar uma expressão condicional na coluna **Condição** da linha da ação **LocalizarPróximoRegistro**.

## <a name="remarks"></a>Comentários

Esta ação equivale a usar o botão **Localizar Próximo** da caixa de diálogo **Localizar e Substituir**.


> [!NOTE]
> <P>[!OBSERVAçãO] Apesar de a ação <STRONG>EncontrarRegistro</STRONG> corresponder ao comando <STRONG>Localizar</STRONG> da guia <STRONG>Página Inicial</STRONG> para tabelas, consultas e formulários, ela não corresponde ao comando <STRONG>Localizar</STRONG> no menu <STRONG>Editar</STRONG> da janela Código. Você não pode usar a ação <STRONG>EncontrarRegistro</STRONG> ou a ação <STRONG>LocalizarPróximoRegistro</STRONG> para pesquisar texto em módulos.</P>




> [!TIP]
> <P>[!DICA] Se você definiu o argumento <STRONG>Somente Campo Atual</STRONG> da ação <STRONG>EncontrarRegistro</STRONG> como <STRONG>Sim</STRONG>, talvez precise usar a ação <STRONG>IrParaControle</STRONG> para mover o foco para o controle que contém os dados que está pesquisando antes de usar a ação <STRONG>LocalizarPróximoRegistro</STRONG>.</P>



Se o texto selecionado no momento for o mesmo do texto de pesquisa quando a ação de macro **LocalizarPróximoRegistro** for executada, a pesquisa começará imediatamente após a seleção, no mesmo campo da seleção e no mesmo registro. Caso contrário, começará no início do registro atual. Isso permite localizar várias instâncias dos mesmos critérios de pesquisa que podem aparecer em um único registro.

Entretanto, observe que, se você usar um botão de comando para executar uma macro que contém a ação **LocalizarPróximoRegistro**, a primeira instância dos critérios de pesquisa será localizada várias vezes. Esse comportamento ocorre porque clicar no botão de comando remove o foco do campo que contém o valor correspondente. A ação **LocalizarPróximoRegistro** começará a pesquisar partindo do início do registro. Para evitar esse problema, execute a macro usando uma técnica que não altera o foco, como um botão de barra de ferramentas personalizado ou uma combinação de teclas definida em uma macro AutoKeys. Como alternativa, defina o foco na macro para o campo que contém os critérios de pesquisa antes de executar a ação **LocalizarPróximoRegistro**.

O mesmo comportamento também ocorre se você usa um botão de comando para executar uma macro que contém a ação **EncontrarRegistro** com o argumento **Localizar Primeiro** definido como **Não**.

Para executar a ação **LocalizarPróximoRegistro** em um módulo do Visual Basic for Applications, use o método **EncontrarPróximo** do objeto **DoCmd**.

