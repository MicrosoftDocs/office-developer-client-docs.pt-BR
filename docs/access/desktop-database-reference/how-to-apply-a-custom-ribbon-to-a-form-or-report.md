---
title: Aplicar uma faixa de opções personalizada a um formulário ou relatório
TOCTitle: Apply a custom ribbon to a form or report
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4fb0155b1a1ed36b6fe924f72a4da385197cc21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464552"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a>Aplicar uma faixa de opções personalizada a um formulário ou relatório


**Aplica-se a**: Access 2013 | Office 2013

A faixa de opções usa marcação XML declarativa baseada em texto que simplifica a criação e a personalização da faixa de opções. Com algumas linhas de XML, você pode criar a interface exata para o usuário. Access oferece flexibilidade na personalização da interface do usuário da faixa de opções. Por exemplo, a marcação de personalização pode ser armazenada em uma tabela, inserida em um procedimento VBA, armazenado em outro banco de dados do Access, ou vinculado a ele, de uma planilha do Excel. Este tópico descreve como aplicar faixas de opções personalizadas ao carregar um formulário ou relatório.

## <a name="making-the-ribbon-customization-xml-available"></a>Disponibilizando o XML de personalização da faixa de opções

**Armazenando o XML de Extensibilidade da Faixa de Opções em uma tabela**

Um método que você pode usar para disponibilizar personalizações da faixa de opção é armazená-las em uma tabela chamada **USysRibbons**, as personalizações poderão ser implementadas sem o uso de macros ou de código VBA.

**USysRibbons** é uma tabela do sistema criada pelo usuário. A tabela deve ser criada usando nomes de coluna específicas para que as personalizações da faixa de opções sejam implementadas. A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.

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
<td><p>Contém o nome da faixa de opções personalizada a ser associado essa personalização</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Memorando</p></td>
<td><p>Contém a faixa de opções Extensibility XML (RibbonX) que define a personalização da faixa de opções</p></td>
</tr>
</tbody>
</table>


**Carregando o XML de Extensibilidade da Faixa de Opções programaticamente**

Você pode usar o método **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** para carregar personalizações da faixa de opções programaticamente. Tipicamente, para criar e disponibilizar a faixa de opções para o aplicativo, primeiro você cria um módulo no banco de dados com um procedimento que chama o método **LoadCustomUI**, passando o nome da faixa de opções e a marcação de personalização do XML.

A marcação XML pode vir de um objeto **Recordset** criado de uma tabela, de uma origem externa ao banco de dados como um arquivo XML analisado em uma cadeia de caracteres ou de uma marcação XML inserida diretamente no procedimento. Você pode criar faixas de opções diferentes usando várias chamadas ao método **LoadCustomUI**, passando marcação XML diferente desde que o nome de cada faixa de opções e o atributo **id** das guias que compõem a faixa de opções sejam exclusivas.

Após a conclusão do procedimento, você cria então uma macro AutoExec que chama o procedimento usando a ação RunCode. Dessa forma, quando o aplicativo for iniciado, o método **LoadCustomUI** será automaticamente executado e todas as faixas de opções personalizadas serão disponibilizadas para o aplicativo.

## <a name="assigning-custom-ribbons-to-forms-or-reports"></a>Atribuindo faixas de opções personalizadas a formulários ou relatórios

1.  Siga o processo descrito anteriormente para disponibilizar a faixa de opções personalizada para o aplicativo.

2.  Abra o formulário ou relatório no modo de Design.

3.  Na guia Design, clique em **Folha de propriedades**.

4.  Na guia **Todas** da janela Propriedade, clique na lista **Nome da Faixa de Opções** e selecione uma Faixa de Opções.

5.  Salve, feche e reabra o formulário ou relatório. A faixa de opções da interface do usuário selecionado é exibida.


> [!NOTE]
> As guias exibidas na interface do usuário da faixa de opções são aditivas. Ou seja, a menos que especificamente ocultar as guias ou definir o atributo *começar do zero* como **True**, as guias exibidas em um formulário ou interface de usuário da faixa de opções do relatório estão além das guias existentes.

> [!NOTE]
> [!OBSERVAçãO] Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


