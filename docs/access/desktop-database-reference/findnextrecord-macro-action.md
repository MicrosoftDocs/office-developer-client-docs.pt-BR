---
title: Ação da macro LocalizarPróximoRegistro
TOCTitle: FindNextRecord macro action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c92a43ce2f4417fde83a544022a90cfca572bf60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292346"
---
# <a name="findnextrecord-macro-action"></a>Ação da macro LocalizarPróximoRegistro


**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **LocalizarPróximoRegistro** para localizar o próximo registro que atende aos critérios especificados pela ação **EncontrarRegistro** anterior ou o valor na caixa de diálogo **Localizar e Substituir** (na guia **Página Inicial**, clique em **Localizar**). Use a ação **LocalizarPróximoRegistro** para pesquisar registros várias vezes. Por exemplo, você pode se mover sucessivamente por todos os registros para buscar um cliente específico.

## <a name="setting"></a>Configuração

A ação **LocalizarPróximoRegistro** não tem nenhum argumento. A ação **LocalizarPróximoRegistro** localiza o próximo registro que atende aos critérios definidos pela ação **EncontrarRegistro** ou na caixa de diálogo **Localizar e Substituir**. Os argumentos da ação **EncontrarRegistro** são compartilhados com as opções na caixa de diálogo **Localizar e Substituir**.

Para definir os critérios de pesquisa, use a ação **EncontrarRegistro**. Normalmente, digita-se uma ação **EncontrarRegistro** em uma macro e usa-se a ação **LocalizarPróximoRegistro** para localizar registros sucessivos que atendem aos mesmos critérios. Para pesquisar registros somente quando um determinado critério é atendido, você pode digitar uma expressão condicional na coluna **Condição** da linha da ação **LocalizarPróximoRegistro**.

## <a name="remarks"></a>Comentários

Esta ação equivale a usar o botão **Localizar Próximo** da caixa de diálogo **Localizar e Substituir**.

> [!NOTE]
> [!OBSERVAçãO] Apesar de a ação **EncontrarRegistro** corresponder ao comando **Localizar** da guia **Página Inicial** para tabelas, consultas e formulários, ela não corresponde ao comando **Localizar** no menu **Editar** da janela Código. Você não pode usar a ação **EncontrarRegistro** ou a ação **LocalizarPróximoRegistro** para pesquisar texto em módulos.

> [!TIP]
> [!DICA] Se você definiu o argumento **Somente Campo Atual** da ação **EncontrarRegistro** como **Sim**, talvez precise usar a ação **IrParaControle** para mover o foco para o controle que contém os dados que está pesquisando antes de usar a ação **LocalizarPróximoRegistro**.

Se o texto selecionado no momento for o mesmo do texto de pesquisa quando a ação de macro **LocalizarPróximoRegistro** for executada, a pesquisa começará imediatamente após a seleção, no mesmo campo da seleção e no mesmo registro. Caso contrário, começará no início do registro atual. Isso permite localizar várias instâncias dos mesmos critérios de pesquisa que podem aparecer em um único registro.

Entretanto, observe que, se você usar um botão de comando para executar uma macro que contém a ação **LocalizarPróximoRegistro**, a primeira instância dos critérios de pesquisa será localizada várias vezes. Esse comportamento ocorre porque clicar no botão de comando remove o foco do campo que contém o valor correspondente. A ação **LocalizarPróximoRegistro** começará a pesquisar partindo do início do registro. Para evitar esse problema, execute a macro usando uma técnica que não altera o foco, como um botão de barra de ferramentas personalizado ou uma combinação de teclas definida em uma macro AutoKeys. Como alternativa, defina o foco na macro para o campo que contém os critérios de pesquisa antes de executar a ação **LocalizarPróximoRegistro**.

O mesmo comportamento também ocorre se você usa um botão de comando para executar uma macro que contém a ação **EncontrarRegistro** com o argumento **Localizar Primeiro** definido como **Não**.

Para executar a ação **LocalizarPróximoRegistro** em um módulo do Visual Basic for Applications, use o método **EncontrarPróximo** do objeto **DoCmd**.

