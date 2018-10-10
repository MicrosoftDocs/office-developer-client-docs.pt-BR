---
title: Conjunto de formulário, relatório e propriedades de controle
TOCTitle: Set form, report, and control properties
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f839ab2e2c6dfab32c49248f1be1878bf289eb6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463142"
---
# <a name="set-form-report-and-control-properties"></a>Conjunto de formulário, relatório e propriedades de controle

**Aplica-se a**: Access 2013 | Office 2013

Cada formulário, relatório, seção e controle tem definições de propriedade que podem ser alteradas para mudar a aparência ou o comportamento daquele item em particular. Visualize e altere as propriedades utilizando a folha de propriedades, uma macro ou o Visual Basic.

## <a name="set-properties"></a>Configurar as propriedades

1. No modo de design do formulário ou no modo de design do relatório, selecione o controle, seção, formulário ou relatório para o qual você deseja definir a propriedade. Você pode selecionar:
    
   - Um ou mais controles. Para selecionar vários controles, mantenha pressionada a tecla SHIFT e clique nos controles ou arraste o ponteiro do mouse sobre os controles que você deseja selecionar. Se você selecionar vários controles, a folha de propriedades exibirá somente aquelas propriedades que os controles selecionados têm em comum.
    
   - Uma seção. Clique no seletor de seção da seção que você deseja selecionar.
    
   - O formulário ou relatório inteiro. Clique no seletor de formulário ou no seletor de relatório no canto superior esquerdo do formulário ou relatório.

2. Exiba a folha de propriedade clicando no objeto ou seção com o botão direito do mouse e clicando, a seguir, em **Propriedades** no menu de atalho ou, então, clicando em **Propriedades** na barra de ferramentas.

3. Clique na propriedade para a qual você deseja definir o valor e, então, siga um dos procedimentos abaixo:
    
   - Na caixa de propriedades, digite a definição ou expressão apropriada.
    
   - Se a caixa de propriedades contiver uma seta, clique sobre a seta e, depois, em um valor da lista.
    
   - Se um botão **Construir** aparecer à direita da caixa de propriedades, clique sobre ele para exibir um construtor ou para exibir uma caixa de diálogo que lhe permita escolher entre vários construtores. Por exemplo, você pode utilizar o Construtor de código, o Construtor de macros ou o Construtor de consultas para definir algumas propriedades.

## <a name="tips"></a>Dicas

- O Microsoft Access oferece uma caixa **Zoom** para a digitação e visualização de expressões ou outras configurações longas de propriedades. Para exibir a caixa **Zoom**, clique em uma caixa de propriedades na folha de propriedades. A seguir, pressione SHIFT+F2 ou clique o botão direito do mouse e, então, clique em **Zoom** no menu de atalho.

- Você pode definir a propriedade **ControlSource** de alguns controles digitando a definição da propriedade no próprio controle.

- Você pode alterar as configurações de propriedade padrão de um tipo de controle para que os controles criados tenham as novas configurações padrão.

- As configurações de propriedade de um controle acoplado podem não corresponder às configurações semelhantes no campo da tabela ou consulta de base ao qual o controle está acoplado. Se as configurações forem diferentes, as configurações do formulário ou relatório substituirão normalmente as da tabela ou consulta. Para obter mais informações sobre como as propriedades são herdadas, consulte Como as propriedades de controle se relacionam com as propriedades em seus campos base.

