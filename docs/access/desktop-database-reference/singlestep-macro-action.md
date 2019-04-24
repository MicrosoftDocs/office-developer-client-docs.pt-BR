---
title: Ação da macro PassoÚnico
TOCTitle: SingleStep macro action
ms:assetid: 2836fe1d-fb9b-6b42-acfd-c52e468161d4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191989(v=office.15)
ms:contentKeyID: 48543855
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm47687
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9e934b290472dc4bb0ad8619b2ada6992b4215c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308628"
---
# <a name="singlestep-macro-action"></a>Ação da macro PassoÚnico

**Aplica-se ao:** Access 2013, Office 2013

Use a ação **PassoAPasso** para pausar a execução da macro e abrir a caixa de diálogo **Macro Passo a Passo**.

## <a name="setting"></a>Configuração

A ação **PassoAPasso** não tem argumentos.

## <a name="remarks"></a>Comentários

- Use a ação **PassoAPasso** para solucionar problemas em uma macro que não esteja funcionando corretamente. Você pode adicionar a ação **PassoAPasso** a uma macro imediatamente antes de uma ação que você suspeite ser a causa do problema. A ação pausará a macro e abrirá a caixa de diálogo **Macro Passo a Passo**. Essa caixa de diálogo exibe informações sobre a ação da macro atual, como nome da macro, todas as condições especificadas, nome da ação, argumentos e, se aplicável, o número do erro. Na caixa de diálogo, clique em **Passo** para avançar para a próxima ação da macro, clique em **Parar Todas as Macros** para interromper a macro atual e todas as outras macros em execução ou clique em **Continuar** para interromper o passo a passo e continuar a operação normal da macro.

- A ação **PassoAPasso** tem efeito similar a clicar em **Passo a Passo** no grupo **Ferramentas** da guia **Design** do Construtor de Macros. A diferença entre fazer isso e executar a ação **PassoAPasso** é que, ao executar a ação, você poderá colocar a ação da macro exatamente onde desejar que um passo a passo comece. Dessa forma, não é preciso passar por todas as ações anteriores para obter aquela que você deseja examinar. Por outro lado, quando você clica em **Passo a Passo** no Construtor de Macros, é preciso fazer isso antes de executar a macro. Nesse caso, o passo a passo começa na primeira ação da macro.

> [!NOTE]
> [!OBSERVAçãO] Se você aplicar o passo a passo do início ao fim de uma macro, mas sem clicar em **Continuar**, o passo a passo ainda estará ativo quando a macro for finalizada. Qualquer macro subsequente que você executar será iniciada no modo passo a passo. Para desativar esse modo, clique em **Continuar** na caixa de diálogo **Macro Passo a Passo** ou, com uma macro aberta no modo de exibição de Design, na guia **Design** do grupo **Ferramentas**, clique em **Passo a Passo** para desmarcá-lo.
