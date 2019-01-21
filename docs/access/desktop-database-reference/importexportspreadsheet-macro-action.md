---
title: Ação da macro ImportarExportarPlanilha
TOCTitle: ImportExportSpreadsheet macro action
ms:assetid: 526aef41-8329-5335-9d16-4d332542a297
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193927(v=office.15)
ms:contentKeyID: 48544846
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm31446
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f910393c6d7a64258e5afc7545641fc5c6778b03
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726005"
---
# <a name="importexportspreadsheet-macro-action"></a>Ação da macro ImportarExportarPlanilha

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **ImportExportSpreadsheet** para importar ou exportar dados entre o banco de dados atual do Access (.mdb ou .accdb) ou um arquivo de projeto do Access (.adp) e de planilha. Também é possível vincular os dados em uma planilha do Microsoft Excel ao banco de dados atual do Microsoft Access. Com uma planilha vinculada, você pode exibir e editar os dados da planilha com o Access e ainda permitir acesso completo aos dados do seu programa de planilha Excel. Você também pode vincular a dados em um arquivo de planilha do Lotus 1-2-3, mas esses dados são somente leitura no Access.

> [!NOTE]
> Essa ação não será permitida se o banco de dados não for confiável. 

## <a name="setting"></a>Configuração

A ação **TransferirPlanilha** tem os seguintes argumentos.

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
<td><p><strong>Tipo de transferência</strong></p></td>
<td><p>O tipo de transferência que você deseja fazer. Selecione <strong>Importar</strong>, <strong>Exportar</strong> ou <strong>Vincular</strong> na caixa <strong>Tipo de Transferência</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Importar</strong>.  </p><p><strong>OBSERVAÇÃO</strong>: O tipo de <STRONG>Link</STRONG> de transferência não tem suporte para projetos do Access (.adp).</p></td>
</tr>
<tr class="even">
<td><p><strong>Tipo de planilha</strong></p></td>
<td><p>O tipo de planilha de onde importar, para onde exportar ou à qual vincular. Você pode selecionar um de vários tipos de planilha na caixa. O padrão é <strong>Pasta de Trabalho do Excel</strong>.  </p><p><strong>Observação</strong>: você pode importar de vincular (somente leitura) aos arquivos do Lotus. WK4, mas você não pode exportar dados do Access nesse formato de planilha. O Access também não oferece suporte para importar, exportar ou vincular dados do Lotus. WKS ou planilhas do Excel versão 2.0 com essa ação. Se você quiser importar ou vincular dados no Excel versão 2.0 ou o formato Lotus. WKS, converta os dados da planilha em uma versão mais recente do Excel ou do Lotus 1-2-3 antes de importar ou vincular os dados no Access.</p>
</td>
</tr>
<tr class="odd">
<td><p><strong>Nome da Tabela</strong></p></td>
<td><p>O nome da tabela do Access para a qual os dados da planilha serão importados, de onde os dados da planilha serão exportados ou para onde os dados da planilha serão vinculados. Você também pode digitar o nome da consulta seleção do Access da qual você deseja exportar dados. Esse é um argumento obrigatório. Se você selecionar <strong>Import</strong> no argumento <strong>Transfer Type</strong>, o Access anexará os dados da planilha a essa tabela caso a tabela já exista. Caso contrário, o Access criará uma nova tabela com os dados da planilha. No Access, você não poderá usar uma instrução SQL para especificar dados a serem exportados quando estiver usando a ação <strong>ImportExportSpreadsheet</strong>. Em vez de usar uma instrução SQL, primeiro você deverá criar uma consulta e então especificar o nome da consulta no argumento <strong>Table Name</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do arquivo</strong></p></td>
<td><p>O nome do arquivo de planilha de onde importar, para onde exportar ou para onde vincular. Inclua o caminho completo. Esse é um argumento obrigatório. O Access criará uma nova planilha quando você exportar dados do Access. Se o nome do arquivo for igual ao nome de uma planilha existente, o Access substituirá a planilha existente, a menos que você esteja exportando para uma pasta de trabalho do Excel versão 5.0 ou posterior. Nesse caso, o Access copiará os dados exportados para a próxima planilha nova disponível na pasta de trabalho. Se você estiver importando de uma planilha do Excel versão 5.0 ou posterior ou vinculando dela, poderá especificar uma planilha em particular usando o argumento <strong>Intervalo</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Tem Nomes de Campo</strong></p></td>
<td><p>Especifique se a primeira linha da planilha contém os nomes dos campos. Se você selecionar <strong>Sim</strong>, o Access usará os nomes dessa linha como nomes de campo na tabela do Access ao importar ou vincular os dados da planilha. Se você selecionar <strong>Não</strong>, o Access tratará a primeira linha como uma linha de dados normal. O padrão é <strong>Não</strong>. Quando você exporta uma tabela ou uma consulta seleção do Access para uma planilha, os nomes de campos serão inseridos na primeira linha da planilha, não importa o que estiver selecionado neste argumento.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Range</strong></p></td>
<td><p>O intervalo de células a serem importadas ou vinculadas. Deixe esse argumento em branco para importar ou vincular a planilha inteira. Você pode digitar o nome de um intervalo da planilha ou especifique o intervalo de células a serem importadas ou vinculadas. Deixe esse argumento em branco para importar ou vincular a planilha inteira. Você pode digitar o nome de um intervalo na planilha ou especificar o intervalo de células a serem importadas ou vinculadas, como A1:E25 (observe que a sintaxe A1..E25 não funciona no Access 97 ou posterior). Se você estiver importando de uma planilha do Excel versão 5.0 ou posterior ou vinculando para uma, poderá usar o nome da planilha como prefixo e um ponto de exclamação; por exemplo, Orçamento!A1:C7.</p><p><strong>Observação</strong>: quando você exporta em uma planilha, você deve deixar esse argumento em branco. Se você inserir um intervalo, a exportação falhará.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode exportar os dados em consultas seleção do Access para planilhas. O Access exporta o conjunto de resultados da consulta, tratando-o como uma tabela.

Os dados da planilha que você anexa a uma tabela existente do Access devem ser compatíveis com a estrutura da tabela.

- Cada campo na planilha deve ser do mesmo tipo de dados que o campo correspondente na tabela.

- Os campos deverão estar na mesma ordem (a menos que você defina o argumento **Tem Nomes de Campo** como **Sim**; nesse caso, os nomes de campo da planilha deverão corresponder aos nomes de campo na tabela).

Essa ação é semelhante a clicar na guia **Dados Externos** e clicar em **Excel** no grupo **Importar** ou **Exportar** ou clicar em **Mais** no grupo **Importar** ou **Exportar** e clicar em **Arquivo do Lotus 1-2-3**. Você pode usar esses comandos para selecionar uma fonte de dados, como o Access, ou digitar um banco de dados, de planilha ou de arquivo de texto. Se você selecionar uma planilha, será exibida uma série de caixas de diálogo ou um assistente do Access será executado, quando você selecionará o nome da planilha e outras opções. Os argumentos da ação **ImportExportSpreadsheet** refletem as opções nessas caixas de diálogo ou nos assistentes.

> [!NOTE]
> Se você consultar ou filtrar uma planilha vinculada, a consulta ou o filtro será sensível a maiúsculas e minúsculas.

Se você vincular a uma planilha do Excel que esteja aberta em modo Editar, o Access aguardará até a planilha do Excel sair do modo Editar antes da conclusão da vinculação; não há tempo limite.

Para executar a ação **ImportExportSpreadsheet** em um módulo do VBA (Visual Basic for Applications) module, use o método **TransferSpreadsheet** do objeto **DoCmd**.

