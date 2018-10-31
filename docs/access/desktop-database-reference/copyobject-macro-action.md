---
title: Ação de macro CopiarObjeto
TOCTitle: CopyObject Macro Action
ms:assetid: 746f61df-d5db-284a-0897-75820c2be11f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195876(v=office.15)
ms:contentKeyID: 48545661
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12836
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 60c0204bd374feaa950d3158873f68127debaf0f
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862545"
---
# <a name="copyobject-macro-action"></a>Ação de macro CopiarObjeto


**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **CopiarObjeto** para copiar o objeto de banco de dados especificado para um banco de dados do Access diferente ou para o mesmo banco de dados ou o projeto do Access com um novo nome. Por exemplo, é possível executar cópia ou backup de um objeto existente em outro banco de dados ou rapidamente criar um objeto semelhante com algumas alterações.


> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.



## <a name="setting"></a>Configuração

A ação **CopiarObjeto** tem os seguintes argumentos.

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
<td><p><strong>Banco de Dados de Destino</strong></p></td>
<td><p>Um caminho e nome de arquivo válidos para o banco de dados de destino. Insira o caminho e nome de arquivo na caixa <strong>Banco de Dados de Destino</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Deixe este argumento em branco se desejar selecionar o banco de dados atual. 

</p>

> [!NOTE]
> Este argumento só está disponível no ambiente de banco de dados do Access. Ao usar esta ação em um ambiente de projeto do Access (.adp), o argumento Banco de Dados de Destino precisa estar em branco.


<p>Se você executar uma macro que contém a ação <strong>CopiarObjeto</strong> em um banco de dados biblioteca e deixar este argumento em branco, o Microsoft Office Access 2007 copiará o objeto para o banco de dados biblioteca.</p></td>
</tr>
<tr class="even">
<td><p><strong>Novo Nome</strong></p></td>
<td><p>Um novo nome para o objeto. Ao copiar para um banco de dados diferente, deixe este argumento em branco para manter o mesmo nome.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Tipo do Objeto de Origem</strong></p></td>
<td><p>O tipo de objeto que deseja copiar. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong>. Para copiar o objeto selecionado no Painel de Navegação, deixe este argumento em branco.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Objeto de Origem</strong></p></td>
<td><p>O nome do objeto a ser copiado. Na caixa <strong>Nome do objeto de origem</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Tipo de objeto de origem</strong> . Na caixa <strong>Nome do objeto de origem</strong> , clique no objeto a ser copiado. Se você deixar vazio o argumento de <strong>Tipo de objeto de origem</strong> , deixe este argumento também em branco. Se você executar uma macro que contém a ação <strong>CopiarObjeto</strong> em um banco de dados biblioteca, o Access procurará o objeto com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você precisa digitar um valor para um dos argumentos **Banco de Dados de Destino** e **Novo Nome** para esta ação, ou ambos.

Se você deixar os argumentos **Tipo do Objeto de Origem** e **Nome do Objeto de Origem** em branco, o Access copiará o objeto selecionado no Painel de Navegação. Para selecionar um objeto no Painel de Navegação, use a ação **SelecionarObjeto** com o argumento No Painel de Navegação definido como **Sim**.

A ação **CopiarObjeto** equivale a seguir estas etapas manualmente:

1.  Selecione um objeto no Painel de Navegação.

2.  On the Home tab, in the Clipboard group, click Copy.

3.  Na mesma guia, clique em **Colar**.A caixa de diálogo **Colar como** é exibida para você poder dar um novo nome ao objeto. A ação **CopiarObjeto** executa todas essas etapas automaticamente.


> [!NOTE]
> [!OBSERVAçãO] Ao copiar páginas de acesso a dados, a ação **CopiarObjeto** copia somente o link para o arquivo .htm associado, e não o arquivo em si.



O caminho e nome de arquivo do banco de dados de destino precisam existir antes de a macro executar a ação **CopiarObjeto**. Se não existirem, o Access exibirá uma mensagem de erro.

Para executar a ação **CopiarObjeto** em um módulo do VBA (Visual Basic for Applications), use o método **CopyObject** do objeto **DoCmd**.

Você também pode copiar manualmente um objeto selecionado no Painel de Navegação, ou um objeto que está aberto no momento, clicando na guia **Arquivo** e clicando em **Salvar como**. Esse comando fará uma cópia do objeto somente no banco de dados atual. Na caixa de diálogo **Salvar como**, digite o nome da cópia e escolha o tipo de objeto no qual ela será salva. Se o objeto original já tiver sido salvo e você salvá-lo no banco de dados atual com o novo nome, a versão original ainda existirá com o antigo nome.

Para copiar manualmente um objeto para um banco de dados diferente do Access:

1.  Na guia **Dados Externos**, no grupo **Exportar**, clique em **Mais** e clique em **Banco de Dados do Access**.

2.  Na caixa de diálogo **Exportar - Banco de Dados do Access**, digite o nome de arquivo do banco de dados de destino.-ou-Clique em **Procurar** para exibir a caixa de diálogo **Salvar Arquivo**, localize o banco de dados de destino e clique em **Salvar**.

3.  Na caixa de diálogo **Exportar - Banco de Dados do Access**, clique em **OK**. A caixa de diálogo **Exportar** será exibida.

4.  Na caixa de diálogo **Exportar**, digite um nome para o objeto no banco de dados de destino. Escolha qualquer opção aplicável, como **Definição e Dados** ou **Somente Definição** para tabelas. Quando tiver concluído, clique em **OK**.

