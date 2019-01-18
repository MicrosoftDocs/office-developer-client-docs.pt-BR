---
title: Converter tabelas, formulários e relatórios do Microsoft Access
TOCTitle: Convert Microsoft Access tables, forms, and reports
description: Alterações introduzidas pelo Microsoft Access 2002 podem afetar o comportamento da sua versão 1. x ou 2.0 aplicativos.
ms:assetid: cc170e62-a663-60e8-4446-07a7a874b747
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834413(v=office.15)
ms:contentKeyID: 48547731
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5187104
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9c1ff7584269ce073a805edf8710bb3ea4eb1a36
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709821"
---
# <a name="convert-microsoft-access-tables-forms-and-reports"></a>Converter tabelas, formulários e relatórios do Microsoft Access

**Aplica-se a**: Access 2013, o Office 2013

Várias alterações introduzidas pelo Microsoft Access 2002 podem afetar o comportamento dos seus aplicativos versão 1.*x* ou 2.0. As seções a seguir fornecem mais informações sobre essas alterações.

## <a name="indexes-and-relationships"></a>Índices e relações

Uma tabela do Microsoft Access pode conter até 32 índices. As tabelas muito complexas que fazem parte de muitas relações podem exceder o limite de índices e você não poderá converter o banco de dados que contém essas tabelas. O mecanismo de banco de dados do Microsoft Access cria índices em ambos os lados das relações entre tabelas. Se o banco de dados não for convertido, exclua algumas relações e tente convertê-lo novamente.

## <a name="the-limittolist-property-of-combo-boxes"></a>A propriedade LimitToList das caixas de combinação

No Microsoft Access 2002 ou posterior, caixas de combinação aceitam valores **Nulos** quando a propriedade **LimitToList** estiver definida como **True** (– 1), se a lista contém valores **Nulos** ou não. Na versão 2.0, uma caixa de combinação com a propriedade **LimitToList** definida como **True** não aceitará um valor **Nulo** a não ser que a lista contenha um valor **Nulo**. Caso queira impedir que os usuários insiram um valor **Nulo** usando uma caixa de combinação, defina a propriedade **Required** do campo na tabela como **Sim**.

## <a name="menus-and-in-place-activation-of-ole-objects"></a>Menus e ativação in-loco de objetos OLE

Para disponibilizar funcionalidade adicional para você ao ativar objetos OLE in-loco, alguns comandos de menu podem ter sido movidos para um menu que não é substituído quando você ativar um servidor OLE.

As macros no seu aplicativo convertido que utilizam uma ação ExecutarItemDoMenu para executar um comando de menu da versão 2.0 quando um componente é ativado não serão afetadas pelas alterações. Os comandos da versão 2.0 são mapeados até seus equivalentes em versões posteriores do Microsoft Access.

## <a name="referencing-a-control-on-a-read-only-form"></a>Fazendo referência a um controle em um formulário somente leitura

No Microsoft Access 2002 ou posterior, você não pode usar uma expressão para referir-se ao valor de um controle em um formulário de somente leitura que esteja acoplado a uma fonte de registros vazia. Em versões anteriores, a expressão retorna um valor **Nulo**. Antes de fazer referência a um controle em um formulário somente leitura, verifique se a fonte de registros do formulário contém registros.

## <a name="date-fields-and-data-entry"></a>Campos Data e entrada de dados

Se você inserir **3/3** em um campo do tipo Data de uma folha de dados de tabela ou formulário, o ano atual será automaticamente adicionado no Access 2002 ou posterior. No entanto, se você inserir **3/3/** no mesmo campo, o Microsoft Access retornará uma mensagem de erro. O último delimitador de data deve ser omitido para que o Microsoft Access converta a data para o formato apropriado.

## <a name="buttons-created-with-the-command-button-wizard"></a>Botões criados com o Assistente de botão de comando

Se você tiver usado o Assistente de Botão de Comando na versão 2.0 ou 7.0 do Microsoft Access para gerar código que iniciava outro aplicativo, você deve excluir o botão e recriá-lo usando o Assistente de Botão de Comando do Microsoft Access 2002 ou posterior.

## <a name="form-and-report-class-modules"></a>Módulos de classe de formulário e relatório

Em versões do Microsoft Access anteriores a 2002, os objetos **Form** e **Report** têm módulos classe associados mesmo que não haja código por trás do objeto. No Microsoft Access 2002 ou posterior, você pode definir a propriedade **HasModule** de um formulário ou relatório como **False**. Quando a propriedade **HasModule** for definida como **False**, o formulário ou relatório ocupará menos espaço em disco e será carregado mais rapidamente porque deixará de ter um módulo classe associado.

## <a name="converted-version-20-report-has-different-margins"></a>Relatório da versão 2.0 convertido tem margens diferentes

Você pode ter problemas ao tentar imprimir ou visualizar um relatório no Microsoft Access 2002 ou posterior, que tenha sido convertido do Microsoft Access 2.0, se o relatório tiver alguma margem definida como 0. Na conversão de um relatório do Microsoft Access 2.0, as margens não são definidas como 0; em vez disso, são definidas com o valor mínimo de margem válido para a impressora padrão. Isso impede que o relatório imprima dados na área não imprimível da impressora.

Para resolver este problema, reduza a largura da coluna, o espaçamento da coluna ou o número de colunas do relatório de tal modo que a largura das colunas mais a largura das margens padrão seja menor ou igual à largura do papel.

## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a>Não é possível usar a propriedade Format para distinguir valores nulos e sequências de caracteres de comprimento zero

Nas versões 1. *x* e 2.0, você pode usar a propriedade **Format** de um controle para exibir valores diferentes para valores **Nulos** e sequências de caracteres de comprimento zero (""). No Microsoft Access 2002 ou posterior, para distinguir entre valores **Nulos** e cadeias de caracteres com comprimento zero em um controle de formulário, defina a propriedade **ControlSource** do controle como uma expressão que verifique se o valor é **Nulo**. Por exemplo, para exibir "Nulo" ou "SCZ" em um controle, defina a propriedade **ControlSource** do controle como a seguinte expressão:

`=IIf(IsNull([MyControl]), "Null", Format([MyControl], "@;ZLS"))`

