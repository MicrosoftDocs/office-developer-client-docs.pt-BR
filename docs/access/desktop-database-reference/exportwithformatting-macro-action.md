---
title: Ação da macro ExportarcomFormatação
TOCTitle: ExportWithFormatting macro action
ms:assetid: 8926dfa3-bf11-30ab-0f85-46f0a4961784
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197066(v=office.15)
ms:contentKeyID: 48546152
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm159503
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: fb633977fcc1b39fc2a5c0bb69523bc93c193695
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293207"
---
# <a name="exportwithformatting-macro-action"></a>Ação da macro ExportarcomFormatação


**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **ExportarcomFormatação** para gerar a saída dos dados do objeto de banco de dados do Microsoft Access especificado (uma folha de dados, um formulário, um relatório, um módulo ou uma página de acesso a dados) para vários formatos de saída.

## <a name="settings"></a>Configurações

A ação **ExportarcomFormatação** tem os seguintes argumentos.

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
<td><p>O tipo de objeto que contém os dados para gerar saída. Clique em <strong>Tabela</strong> (para uma folha de dados de tabela), <strong>Consulta</strong> (para uma folha de dados de consulta), <strong>Formulário</strong> (para um formulário ou uma folha de dados de formulário), <strong>Relatório</strong>, <strong>Módulo</strong>, <strong>Modo de Exibição de Servidor</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Não é possível gerar saída de uma macro. Se desejar gerar saída do objeto ativo, selecione seu tipo com este argumento, mas deixe o argumento <strong>Nome do Objeto</strong> em branco. Esse é um argumento obrigatório. O padrão é <strong>Tabela</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Objeto</strong></p></td>
<td><p>O nome do objeto que contém os dados de saída. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Object Type</strong>. Se você executar uma macro que contém a ação <strong>ExportWithFormatting</strong> em um banco de dados biblioteca, o Access primeiro procurará o objeto com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Formato de Saída</strong></p></td>
<td><p>O tipo de formato que será usado para gerar saída dos dados. Você pode selecionar <strong>Pasta de Trabalho do Excel 97 - Excel 2003 (*.xls)</strong>, <strong>Pasta de Trabalho Binária do Excel (*.xlsb)</strong>, <strong>Pasta de Trabalho do Excel (*.xlsx)</strong>, <strong>HTML (*.htm; *.html)</strong>, <strong>Pasta de Trabalho do Microsoft Excel 5.0/95 (*.xls)</strong>, <strong>Formato PDF (*.pdf)</strong>, <strong>Formato Rich Text (*.rtf)</strong>, <strong>Arquivos de Texto (*.txt)</strong> ou <strong>Formato XPS (*.xps)</strong>. Se você deixar este argumento em branco, o Access solicitará o formato de saída.</p></td>
</tr>
<tr class="even">
<td><p><strong>Arquivo de saída</strong></p></td>
<td><p>O arquivo de destino da saída dos dados, incluindo o caminho completo. Você pode incluir a extensão de nome de arquivo padrão para o formato de saída selecionado com o argumento <strong>Formato de Saída</strong>, mas ele não é obrigatório. Se você deixar o argumento <strong>Arquivo de Saída</strong> em branco, o Access solicitará um nome de arquivo de saída.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Início Automático</strong></p></td>
<td><p>Especifica se o software apropriado deverá ser iniciado imediatamente após a execução da ação <strong>ExportarcomFormatação</strong>, com o arquivo especificado pelo argumento <strong>Arquivo de Saída</strong> aberto.</p></td>
</tr>
<tr class="even">
<td><p><strong>Arquivo de Modelo</strong></p></td>
<td><p>O caminho e o nome de um arquivo que será usado como modelo para arquivos HTML. O arquivo modelo é um arquivo de texto que inclui marcas HTML e tokens que são exclusivos do Access.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Codificação</strong></p></td>
<td><p>O tipo de formato de codificação de caracteres usado para gerar saída de texto ou de dados HTML. Você pode selecionar <strong>MS-DOS</strong>, <strong>Unicode</strong> ou <strong>Unicode (UTF-8)</strong>. A configuração de argumento <strong>MS-DOS</strong> está disponível somente para arquivos de texto. Se você deixar este argumento em branco, o Access gerará saída dos dados usando a codificação padrão do Windows para arquivos de texto e a codificação de sistema padrão para arquivos HTML.</p></td>
</tr>
<tr class="even">
<td><p><strong>Qualidade da Saída</strong></p></td>
<td><p>Selecione <strong>Imprimir</strong> para otimizar a saída para impressão ou <strong>Tela</strong> para otimizar a saída para exibição na tela.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Os dados do Access têm saída no formato selecionado e podem ser lidos por qualquer programa que use o mesmo formato. Por exemplo, é possível gerar saída de um relatório do Access com sua formatação para um documento de Formato Rich Text e abrir o documento no Microsoft Word.

Se você gerar saída do objeto de banco de dados para o formato HTML, o Access criará um arquivo em formato HTML que contém os dados do objeto. Você pode usar o argumento **Arquivo Modelo** para especificar um arquivo que será usado como modelo para o arquivo .html.

As regras a seguir se aplicam ao usar a ação **ExportarcomFormatação** para gerar saída de um objeto de banco de dados para quaisquer dos formatos de saída:

  - É possível gerar saída dos dados em folhas de dados de tabela, de consulta e de formulário. No arquivo de saída, todos os campos da folha de dados aparecem da mesma maneira que no Access, com a exceção dos campos que contêm objetos OLE. As colunas dos campos de objetos OLE são incluídas no arquivo de saída, mas os campos ficam em branco.

  - Para um controle que é ligado a um campo Sim/Não (um botão de alternância, um botão de opções ou uma caixa de seleção), o arquivo de saída exibe o valor -1 (Sim) ou 0 (Não).

  - Para uma caixa de texto ligada a um campo de hiperlink, o arquivo de saída exibe o hiperlink para todos os formatos de saída com exceção de texto MS-DOS (nesse caso, o hiperlink é exibido como texto normal).

  - Se você gerar saída dos dados de um formulário em modo Formulário, o arquivo de saída sempre conterá o modo Folha de Dados do formulário.

  - Quando é gerada saída de uma folha de dados, um formulário ou uma página de acesso a dados em formato HTML, um arquivo .html é criado. Quando é gerada saída de um relatório em formato HTML, um arquivo .html é criado para cada página do relatório.

O resultado da execução da ação **ExportarcomFormatação** é semelhante a clicar em uma das opções do grupo **Exportar** da guia **Dados Externos**. Os argumentos da ação correspondem às configurações da caixa de diálogo **Exportar**.

Para executar a ação **ExportarcomFormatação** em um módulo do VBA (Visual Basic for Applications), use o método **SaídaPara** do objeto **DoCmd**.

