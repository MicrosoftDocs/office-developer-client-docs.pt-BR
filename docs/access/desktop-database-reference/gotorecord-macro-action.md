---
title: Ação da macro IrParaRegistro
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7534ae84b57d14450009865ea330a4c54d4cfb44
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708477"
---
# <a name="gotorecord-macro-action"></a>Ação da macro IrParaRegistro


**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **IrParaRegistro** para tornar o registro especificado no registro atual de um conjunto de resultados de tabela, formulário, ou consulta aberta.

## <a name="setting"></a>Configuração

A ação **IrParaRegistro** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Tipo de Objeto</strong></p></td>
<td><p>O tipo de objeto que contém o registro que você deseja tornar no atual. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Deixe este argumento em branco para selecionar o objeto ativo.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Objeto</strong></p></td>
<td><p>O nome do objeto que contém o registro que você deseja tornar no registro atual. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados atual do tipo selecionado pelo argumento <strong>Tipo de Objeto</strong>. Se você deixar o argumento <strong>Tipo de Objeto</strong> em branco, deixe este argumento em branco também.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>O registro que se tornará o atual. Clique em <strong>Anterior</strong>, <strong>Próximo</strong>, <strong>Primeiro</strong>, <strong>Último</strong>, <strong>Ir Para</strong> ou <strong>Novo</strong> na caixa <strong>Registro</strong>. O padrão é <strong>Não</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Offset</strong></p></td>
<td><p>Um inteiro ou uma expressão que é avaliada como um número inteiro. Uma expressão deve ser precedida por um sinal de igualdade (<strong>=</strong>). Este argumento especificará o registro para tornar o registro atual. Você pode usar o argumento <strong>deslocamento</strong> de duas maneiras:</p>
<ul>
<li><p>Quando o argumento <strong>Registro</strong> é <strong>Próximo</strong> ou <strong>Anterior</strong>, o Microsoft Office Access 2007 move para frente ou para trás o número de registros especificado no argumento <strong>Deslocamento</strong>.</p></li>
<li><p>Quando o argumento <strong>Registro</strong> é <strong>Ir Para</strong>, o Access se move para o registro com o número igual ao do argumento <strong>Deslocamento</strong>. O número de registros é mostrado na caixa de número de registros na parte inferior da janela.</p>
<p><strong>Observação</strong>: se você usar o <strong>primeiro</strong>, <strong>último</strong>ou <strong>novo</strong> a definição do argumento <strong>registro</strong> , o Access ignora o argumento <strong>deslocamento</strong> . Se você inserir um argumento <strong>deslocamento</strong> muito grande, o Access exibe uma mensagem de erro. Você não pode inserir números negativos para o argumento <strong>deslocamento</strong> .</p></li>
<li><p>Quando o argumento <strong>Registro</strong> é <strong>Próximo</strong> ou <strong>Anterior</strong>, o Microsoft Office Access 2007 move para frente ou para trás o número de registros especificado no argumento <strong>Deslocamento</strong>.</p></li>
<li><p>Quando o argumento <strong>Registro</strong> é <strong>Ir Para</strong>, o Access se move para o registro com o número igual ao do argumento <strong>Deslocamento</strong>. O número de registros é mostrado na caixa de número de registros na parte inferior da janela.</p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se o foco for um controle específico em um registro, esta ação vai deixá-lo no mesmo controle do novo registro.

Você pode usar a configuração **Novo** do argumento **Registro** para se mover para o registro em branco ao final de um formulário ou tabela para poder inserir novos dados.

Esta ação é semelhante a clicar na seta abaixo do botão **Localizar** da guia **Página Inicial** e clicar em **Ir Para**. Os subcomandos **Primeiro**, **Último**, **Próximo**, **Anterior** e **Novo Registro** do comando **Ir Para** têm no objeto selecionado o mesmo efeito das configurações **Primeiro**, **Último**, **Próximo**, **Anterior** e **Novo** do argumento **Registro**. Você também pode se mover para os registros usando os botões de navegação na parte inferior da janela.

Você poderá usar a ação **IrParaRegistro** para tornar um registro de um formulário oculto no registro atual se especificar o formulário oculto nos argumentos **Tipo de Objeto** e **Nome do Objeto**.

Para executar a ação **IrParaRegistro** em um módulo do VBA (Visual Basic for Applications), use o método **GoToRecord** do objeto **DoCmd**.

