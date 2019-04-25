---
title: Aplicar uma faixa de opções personalizada a um formulário ou relatório
TOCTitle: Apply a custom ribbon to a form or report
description: Como aplicar uma faixa de opções personalizada ao carregar um formulário ou relatório no Access 2013.
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 329f184a1bcd3c856ccfd0b15c3fa92bc6230c98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291912"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a>Aplicar uma faixa de opções personalizada a um formulário ou relatório

**Aplica-se ao**: Access 2013, Office 2013

A faixa de opções usa marcação XML declarativa baseada em texto que simplifica a criação e a personalização da faixa de opções. Com algumas linhas de XML, você pode criar a interface exata para o usuário. O Access oferece flexibilidade na personalização da interface do usuário da faixa de opções. 

Por exemplo, a marcação de personalização pode ser armazenada em uma tabela, inserida em um procedimento VBA, armazenado em outro banco de dados do Access, ou vinculado a ele, de uma planilha do Excel. Este tópico descreve como aplicar uma faixa de opções personalizada ao carregar um formulário ou relatório.

## <a name="make-the-ribbon-customization-xml-available"></a>Disponibilizar o XML da personalização da faixa de opções

### <a name="store-ribbon-extensibility-xml-in-a-table"></a>Armazenar o XML da extensibilidade da faixa de opções em uma tabela

Um método que você pode usar para disponibilizar personalizações da faixa de opção é armazená-las em uma tabela chamada **USysRibbons**, as personalizações poderão ser implementadas sem o uso de macros ou de código VBA.

**USysRibbons** sistema de tabela criado pelo usuário. A tabela deve ser criada usando nomes de coluna específicas para que as personalizações da faixa de opções sejam implementadas. 

A tabela a seguir lista as configurações para usar ao criar a tabela **USysRibbons**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da coluna</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>Texto</p></td>
<td><p>Contém o nome da faixa de opções personalizada a ser associado à esta personalização.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Memorando</p></td>
<td><p>Contém o XML de extensibilidade da Faixa de Opções (RibbonX) que define a personalização da faixa de opções.</p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a>Carrega programática XML da extensibilidade da faixa de opções

Você pode usar o método **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** para carregar personalizações da faixa de opções programaticamente. Tipicamente, para criar e disponibilizar a faixa de opções para o aplicativo, primeiro você cria um módulo no banco de dados com um procedimento que chama o método **LoadCustomUI**, passando o nome da faixa de opções e a marcação de personalização do XML.

A marcação XML pode vir de um objeto **Recordset** criado de uma tabela, de uma origem externa ao banco de dados como um arquivo XML analisado em uma cadeia de caracteres ou de uma marcação XML inserida diretamente no procedimento. Você pode criar faixas de opções diferentes usando várias chamadas ao método **LoadCustomUI**, passando marcação XML diferente desde que o nome de cada faixa de opções e o atributo **id** das guias que compõem a faixa de opções sejam exclusivas.

Após a conclusão do procedimento, você cria então uma macro AutoExec que chama o procedimento usando a ação RunCode. Dessa forma, quando o aplicativo for iniciado, o método **LoadCustomUI** será automaticamente executado e todas as faixas de opções personalizadas serão disponibilizadas para o aplicativo.

## <a name="assign-custom-ribbons-to-forms-or-reports"></a>Atribuir faixas de opções personalizadas a formulários e relatórios

1.  Siga o processo descrito anteriormente para disponibilizar a faixa de opções personalizada para o aplicativo.

2.  Abra o formulário ou relatório no modo Design.

3.  Na guia Design, escolha **Folha de Propriedades**.

4.  Na guia **Todas** da janela Propriedade, escolha a lista **Nome da Faixa de Opções** e selecione uma Faixa de Opções.

5.  Salve, feche e reabra o formulário ou relatório. A faixa de opções da interface do usuário selecionada é exibida.


> [!NOTE]
> As guias exibidas na faixa de opções da interface do usuário são aditivas. Isso quer dizer que, a menos que você oculte especificamente as guias ou defina o atributo *Start from Scratch* como **Verdadeiro**, as guias exibidas na Faixa de Opções da interface do usuário de um formulário ou relatório são adicionais ás guias existentes.

> [!NOTE]
> Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


