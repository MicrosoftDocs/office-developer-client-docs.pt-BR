---
title: 'HelloData: um aplicativo ADO simples'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7d9be9b91b3f847516eb3c22aa37e46c8a551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292017"
---
# <a name="hellodata-a-simple-ado-application"></a>HelloData: um aplicativo ADO simples

**Aplica-se ao:** Access 2013, Office 2013

Para preparar a infraestrutura para uma exploração da biblioteca do ADO, considere um aplicativo ADO simples, denominado "HelloData." Esse aplicativo consulta por etapas cada uma das quatro operações principais do ADO (obtenção, exame, edição e atualização de dados). Para enfocar os conceitos básicos do ADO e impedir a desordem de códigos será feito um tratamento mínimo de erros no exemplo.

O aplicativo consulta o banco de dados de exemplo Northwind, incluído no Microsoft SQL Server 2000.

**Para executar o HelloData**

1.  Crie um novo Projeto Executável Padrão do Visual Basic que faça referências à biblioteca do ADO 2.5.

2.  Crie quatro botões de comando na parte superior do formulário, definindo as propriedades **Name** e **Caption** como os valores mostrados na tabela a seguir.

3.  Debaixo dos botões, adicione **Microsoft DataGrid Control** (Msdatgrd.ocx). O arquivo Msdatgrd. ocx é fornecido com o Visual Basic e está localizado \\em\\seu diretório \\Windows\\system32 ou winnt system32. Para adicionar o controle DataGrid ao painel da caixa de ferramentas do Visual Basic, selecione **Componentes...** no menu **Projeto**. Depois, verifique a caixa próxima a "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" e clique em **OK**. Para adicionar o controle ao projeto, arraste o controle DataGrid da Caixa de Ferramentas para o formulário do Visual Basic.

4.  Crie uma **TextBox** no formulário abaixo da grade e defina as propriedades como mostra a tabela. O formulário deverá ter uma aparência semelhante à figura a seguir, quando você tiver finalizado.

5.  Por fim, copie o código listado no [código HelloData](hellodata-code.md) e cole-o na janela do editor de código do formulário. Pressione **F5** para executar o código.

> [!NOTE]
> [!OBSERVAçãO] No exemplo a seguir e por todo o guia, o id de usuário "MyId" com a senha "123aBc" será usado para se autenticar no servidor. Você deve substituir esses valores com as credenciais de logon válidas do servidor. Além disso, substitua o valor "MyServer" pelo nome do seu servidor.

Para obter uma descrição detalhada do código, consulte [HelloData Details](hellodata-details.md).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de controle</p></th>
<th><p>Propriedade	</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Formulário</p></td>
<td><p>Nome</p></td>
<td><p>Form1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Altura</p></td>
<td><p>6500</p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p>Largura</p></td>
<td><p>6500</p></td>
</tr>
<tr class="even">
<td><p>MS DataGrid</p></td>
<td><p>Nome</p></td>
<td><p>grdDisplay1</p></td>
</tr>
<tr class="odd">
<td><p>TextBox</p></td>
<td><p>Nome</p></td>
<td><p>txtDisplay1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Multiline</p></td>
<td><p>verdadeiro</p></td>
</tr>
<tr class="odd">
<td><p>Botão de Comando</p></td>
<td><p>Nome</p></td>
<td><p>cmdGetData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Legenda</p></td>
<td><p>Get Data</p></td>
</tr>
<tr class="odd">
<td><p>Botão de Comando</p></td>
<td><p>Nome</p></td>
<td><p>cmdExamineData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Legenda</p></td>
<td><p>Examine Data</p></td>
</tr>
<tr class="odd">
<td><p>Botão de Comando</p></td>
<td><p>Nome</p></td>
<td><p>cmdEditData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Legenda</p></td>
<td><p>Edit Data</p></td>
</tr>
<tr class="odd">
<td><p>Botão de Comando</p></td>
<td><p>Nome</p></td>
<td><p>cmdUpdateData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Legenda</p></td>
<td><p>Update Data</p></td>
</tr>
</tbody>
</table>



