---
title: Ação de macro MinimizarJanela
TOCTitle: MinimizeWindow Macro Action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8ff22b21bfc411f536b780d74a0c2b62a396a4cf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465472"
---
# <a name="minimizewindow-macro-action"></a>Ação de macro MinimizarJanela


**Aplica-se a**: Access 2013 | Office 2013

Se o Access estiver configurado para usar janelas sobrepostas em vez de documentos com guias, você pode usar a ação **Minimizarjanela** para reduzir a janela ativa para uma barra de título pequena na parte inferior da janela do Access.


> [!NOTE]
> <P>[!OBSERVAçãO] Esta ação não pode ser aplicada a janelas de código no Editor do Visual Basic (VBE). Para obter informações sobre como afetar janelas de código, consulte o tópico da propriedade <STRONG>WindowState</STRONG>.</P>



## <a name="setting"></a>Configuração

A ação **MinimizarJanela** não tem nenhum argumento.

## <a name="remarks"></a>Comentários

Você pode usar esta ação para remover uma janela da tela enquanto deixa o objeto aberto. Também pode usar esta ação para abrir um objeto sem exibir sua janela. Para exibir o objeto, use a ação **SelecionarObjeto** com a ação **MaximizarJanela** ou **Restaurar**. A ação **RestaurarJanela** restaura uma janela minimizada para o tamanho anterior.

A ação **MinimizarJanela** equivale a clicar no botão **Minimizar** no canto superior direito da janela ou clicar em **Minimizar** no menu **Controle** da janela.

**Dicas**

  - Talvez seja necessário primeiro usar a ação **SelecionarObjeto** se a janela a ser minimizada não for a janela ativa.

  - Para ocultar o Painel de Navegação, use a ação **SelecionarObjeto** com o argumento do Painel de Navegação definido como **Sim** e use a ação **MinimizarJanela**. O objeto selecionado na ação **SelecionarObjeto** pode ser qualquer objeto no banco de dados.

  - Você pode ocultar a janela ativa clicando em **Gerenciar Esta Janela** no menu **Exibir** e clicando em **Ocultar**. Em vez de ser reduzida a um ícone, a janela ficará invisível. Use o comando **Reexibir** no mesmo menu para que a janela reapareça. É possível usar a ação **ExecutarComandodeMenu** para executar qualquer um desses comandos com uma macro.

  - Você também pode usar a ação **DefinirValor** para definir a propriedade **Visível** de um formulário para ocultar ou mostrar a janela do formulário.

Para executar a ação **MinimizarJanela** em um módulo do VBA (Visual Basic for Applications), use o método **Minimizar** do objeto **DoCmd**.

