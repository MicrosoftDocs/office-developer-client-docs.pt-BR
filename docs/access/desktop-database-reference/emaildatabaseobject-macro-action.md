---
title: Ação da macro EnviarObjetodeBancodeDadosporEMail
TOCTitle: EMailDatabaseObject macro action
ms:assetid: 7fd80596-5c08-dab9-5343-c0edc38a1af9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196469(v=office.15)
ms:contentKeyID: 48545915
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm24439
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f0c0ba73274d6f27a9e2a857aea1061416168f3a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922913"
---
# <a name="emaildatabaseobject-macro-action"></a>Ação da macro EnviarObjetodeBancodeDadosporEMail

**Aplica-se a:** Access 2013 | Office 2013

Você pode usar a ação **EMailDatabaseObject** para incluir a folha de dados especificada do Microsoft Access, o formulário, o relatório, o módulo ou a página de acesso a dados em uma mensagem eletrônica de email, onde ela possa ser visualizada e encaminhada.

> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.

## <a name="settings"></a>Configurações

A ação **EnviarObjetodeBancodeDadosporEMail** tem os seguintes argumentos.

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
<td><p><strong>Tipo de objeto</strong></p></td>
<td><p>O tipo de objeto a ser incluído na mensagem de email. Clique em <strong>Tabela</strong> (para obter uma folha de dados da tabela), <strong>Consulta</strong> (para obter uma folha de dados da consulta), <strong>Formulário</strong> (para obter um formulário ou uma folha de dados do formulário), <strong>Relatório</strong>, <strong>Módulo</strong> ou <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Procedimentos Armazenados</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Não é possível enviar uma macro. Se quiser incluir o objeto ativo, selecione o respectivo tipo com esse argumento, mas deixe em branco o argumento <strong>Nome do objeto</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do objeto</strong></p></td>
<td><p>O nome do objeto para incluir na mensagem de email. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Object Type</strong>. Se você deixar os argumentos <strong>Object Type</strong> e o <strong>Object Name</strong> em branco, o Access enviará uma mensagem ao aplicativo de email sem nenhum objeto banco de dados. Se você executar uma macro que contém a ação ￼ <strong>EMailDatabaseObject</strong> em um banco de dados da biblioteca, o Access primeiro procurará o objeto com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Formato de Saída</strong></p></td>
<td><p>O tipo de formato a ser utilizado para o objeto incluído. A lista dos formatos que você pode selecionar dentre será alterada dependendo se você selecionar para o argumento de <strong>Tipo de objeto</strong> . Formatos disponíveis podem incluir <strong>Excel 97 - pasta de trabalho do Excel 2003 (*. xls)</strong>, a <strong>Pasta de trabalho binária do Excel (*. xlsb)</strong>, a <strong>Pasta de trabalho do Excel (*. xlsx)</strong>, <strong>HTML (*. htm, *. HTML)</strong>, <strong>Pasta de trabalho do Microsoft Excel 5.0/95 (*. xls)</strong>, <strong>formato PDF </strong>, <strong>Formatar Rich Text (RTF)</strong>, <strong>arquivos de texto (*. txt)</strong>ou <strong>formato XPS (*. XPS)</strong>. Na caixa <strong>Formato de saída</strong> . Módulos podem ser enviados somente no formato de texto. Páginas de acesso a dados só podem ser enviadas no formato HTML. Se você deixar este argumento em branco, o Access solicitará o formato de saída.</p></td>
</tr>
<tr class="even">
<td><p><strong>To</strong></p></td>
<td><p>Os destinatários cujos nomes você deseja inserir na linha <strong>Para</strong> da mensagem de email. Se você deixar este argumento em branco, o Access solicitará os nomes dos destinatários. Separe os nomes dos destinatários especificados nesse argumento (e nos argumentos <strong>Cc</strong> e <strong>Cco</strong>) usando um ponto e vírgula (;) ou com o separador de lista definido na guia <strong>Número</strong> da caixa de diálogo <strong>Propriedades das Configurações Regionais</strong> no <strong>Painel de Controle</strong> do Windows. Se o aplicativo de email não identificar os nomes dos destinatários, a mensagem não será enviada e ocorrerá um erro.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Cc</strong></p></td>
<td><p>Os destinatários da mensagem cujos nomes você deseja colocar na <strong>Cc</strong> (&quot;cópia carbono&quot;) linha na mensagem de email. Se você deixar este argumento em branco, a linha <strong>Cc</strong> da mensagem de email ficará em branco.</p></td>
</tr>
<tr class="even">
<td><p><strong>Cco</strong></p></td>
<td><p>Os destinatários da mensagem cujos nomes você deseja colocar na <strong>Cco</strong> (&quot;cópia oculta&quot;) linha na mensagem de email. Se você deixar este argumento em branco, a linha <strong>Cco</strong> ficará em branco.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Assunto</strong></p></td>
<td><p>O assunto da mensagem. Esse texto aparece na linha <strong>Assunto</strong> da mensagem de email. Se você deixar este argumento em branco, a linha <strong>Assunto</strong> ficará em branco.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Texto da mensagem</strong></p></td>
<td><p>Qualquer texto que você quiser incluir na mensagem, adicionalmente ao objeto de banco de dados. Esse texto aparece no corpo principal da mensagem de email, depois do objeto. Se você deixar este argumento em branco, nenhum texto adicional será incluído na mensagem de email. Se deixar em branco os argumentos <strong>Tipo de objeto</strong> e <strong>Nome do objeto</strong>, você poderá usar este argumento para enviar uma mensagem de email sem um objeto de banco de dados.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Editar mensagem</strong></p></td>
<td><p>Especifica se a mensagem pode ser editada antes do envio. Se você selecionar <strong>Sim</strong>, o aplicativo de email será iniciado automaticamente e a mensagem poderá ser editada. Se escolher <strong>Não</strong>, a mensagem será enviada sem que o usuário tenha a oportunidade de editá-la. O padrão é <strong>Sim</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Arquivo de Modelo</strong></p></td>
<td><p>O caminho e o nome do arquivo que você deseja usar como modelo para um arquivo HTML. O arquivo de modelo contém marcas HTML.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O objeto na mensagem de email está no formato de saída selecionado. Quando você clica duas vezes no objeto, o software adequado é iniciado com o objeto aberto.

As regras a seguir são aplicáveis quando você usa a ação **EnviarObjetodeBancodeDadosporEMail** para incluir um objeto de banco de dados em uma mensagem de email:

- Você pode enviar uma tabela, uma consulta e folhas de dados de formulário. No objeto incluído, todos os campos da folha de dados mantêm a mesma aparência do Access, exceto os campos que contêm objetos OLE. As colunas desses campos estão incluídas no objeto, mas os campos estão em branco.

- Para um controle acoplado a um campo Sim/Não (um botão de alternância, um botão de opção ou uma caixa de seleção), o arquivo de saída exibe o valor –1 (Sim) ou 0 (Não).

- Para uma caixa de texto acoplada a um campo Hiperlink, o arquivo de saída exibe o hiperlink para todos os formatos de saída, exceto o texto MS-DOS (nesse caso, o hiperlink é exibido apenas como texto normal).

- Se você enviar um formulário no modo Formulário, o objeto incluído sempre conterá o modo Folha de Dados do formulário.

- Se você enviar um relatório, os únicos controles incluídos no objeto serão caixas de texto e, em alguns casos, rótulos. Todos os outros controles serão ignorados. As informações de cabeçalho e rodapé também não serão incluídas. A única exceção é que, quando você envia um relatório no formato Excel, uma caixa de texto em um rodapé de grupo, contendo uma expressão com a função **Soma**, é incluída no objeto. Nenhum outro controle em um cabeçalho ou em um rodapé (e nenhuma outra função de agregação além de **Soma**) será incluído no objeto.

- Os sub-relatórios estão incluídos no objeto.

- Quando você enviar uma folha de dados, um formulário ou uma página de acesso a dados no formato HTML, será criado um arquivo .html. Quando enviar um relatório no formato HTML, será criado um arquivo .html para cada página do relatório.

Para executar a ação **EnviarObjetodeBancodeDadosporEMail** em um módulo do VBA (Visual Basic for Applications), use o método **EnviarObjeto** do objeto **DoCmd**.

### <a name="about-the-contributor"></a>Sobre o colaborador

**Link fornecido pelo** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), o fundador e presidente da FMS, Inc., uma fornecedora de soluções de banco de dados personalizado e ferramentas de desenvolvedor.

  - [Recursos e limites do uso do Método SendObject para envio](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





