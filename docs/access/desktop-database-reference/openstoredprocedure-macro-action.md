---
title: Ação de macro AbrirProcedimentoArmazenado
TOCTitle: OpenStoredProcedure Macro Action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8b30049348171fcd65bbc2edd25c18256a12c955
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463319"
---
# <a name="openstoredprocedure-macro-action"></a>Ação de macro AbrirProcedimentoArmazenado


**Aplica-se a**: Access 2013 | Office 2013

Em um projeto do Access, você pode usar a ação **AbrirProcedimentoArmazenado** para abrir um procedimento armazenado em modo Folha de Dados, em modo Design de procedimento armazenado ou Visualizar Impressão. Esta ação executa o procedimento armazenado nomeado quando aberta em modo Folha de Dados. Você pode selecionar o modo de entrada de dados do procedimento armazenado e restringir os registros exibidos pelo procedimento armazenado.


> [!NOTE]
> <P>[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</P>



## <a name="setting"></a>Configuração

A ação **AbrirProcedimentoArmazenado** tem os seguintes argumentos.

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
<td><p><strong>Nome do Procedimento</strong></p></td>
<td><p>O nome do procedimento armazenado para abrir. A caixa <strong>Nome do procedimento</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todos os procedimentos armazenados no banco de dados atual. Este é um argumento obrigatório. Se você executar uma macro que contém a ação <strong>AbrirProcedimentoArmazenado</strong> em um banco de dados biblioteca, o Microsoft Access procurará o procedimento armazenado com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>O modo de exibição no qual o procedimento armazenado será aberto. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de Dados</strong></p></td>
<td><p>O modo de entrada de dados do procedimento armazenado. Isso se aplica somente a procedimentos armazenados abertos no modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode exibir ou editar os existentes), <strong>Editar</strong> (o usuário pode exibir ou editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Esta ação é semelhante a clicar duas vezes no procedimento armazenado do Painel de Navegação ou a clicar com o botão direito do mouse no procedimento armazenado do Painel de Navegação e selecionar o comando desejado.

Alternar para o modo Design enquanto o procedimento armazenado é aberto remove a configuração do argumento **Modo de Dados** do procedimento armazenado. Essa configuração não entra em vigor, mesmo se o usuário retorna para o modo Folha de Dados.


> [!TIP]
> <P></P>
> <UL>
> <LI>
> <P>Você pode arrastar um procedimento armazenado no painel de navegação para uma linha de ação de macro. Isso cria automaticamente uma ação <STRONG>AbrirProcedimentoArmazenado</STRONG> que abre o procedimento armazenado no modo folha de dados.</P>
> <LI>
> <P>
> 						Se você não deseja exibir as mensagens do sistema que normalmente aparecem quando um procedimento armazenado é executado (indicando que ele é um procedimento armazenado e mostrando quantos registros serão afetados), use a ação <STRONG>DefinirAviso</STRONG> para suprimir a exibição dessas mensagens.
</P></LI></UL>
<P></P>



Para executar a ação **AbrirProcedimentoArmazenado** em um módulo do VBA (Visual Basic for Applications), use o método **OpenStoredProcedure** do objeto **DoCmd**.

