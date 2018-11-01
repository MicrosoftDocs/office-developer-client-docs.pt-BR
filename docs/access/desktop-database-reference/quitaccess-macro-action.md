---
title: Ação de macro SairdoAccess
TOCTitle: QuitAccess Macro Action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d26f8d32e0df350c52ea22dfec44ac7a24c9ecc9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870748"
---
# <a name="quitaccess-macro-action"></a>Ação de macro SairdoAccess


**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **SairdoAccess** para sair do Microsoft Access. A ação **SairdoAccess** também pode especificar uma das várias opções para salvar objetos de banco de dados antes de sair do Access.


> [!NOTE]
> <P>[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</P>



## <a name="setting"></a>Configuração

A ação **SairdoAccess** tem os seguintes argumentos.

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
<td><p><strong>Options</strong></p></td>
<td><p>Especifica o que acontece com objetos não salvos ao encerrar o Access. Clique em <strong>Aviso</strong> (para exibir caixas de diálogo que perguntam se cada objeto será salvo), <strong>Salvar Tudo</strong> (para salvar todos os objetos sem avisar por caixas de diálogo) ou <strong>Sair</strong> (para encerrar sem salvar nenhum objeto) na caixa <strong>Opções</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Salvar Tudo</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O Access não executa nenhuma ação que siga a ação **SairdoAccess** em uma macro.

Você pode usar esta ação para encerrar o Access sem avisos de caixas de diálogo **Salvar** usando um comando de menu personalizado ou um botão de um formulário. Por exemplo, talvez você tenha um formulário mestre usado para exibir os objetos em seu espaço de trabalho personalizado. Esse formulário pode ter um botão **Encerrar** que executa uma macro que contém a ação **SairdoAccess** com o argumento **Opções** definido como **Salvar Tudo**.

Esta ação equivale a clicar na guia **Arquivo** e clicar em **Sair**. Se você tiver objetos não salvos ao clicar nesse comando, as caixas de diálogo que aparecerem serão as mesmas daquelas exibidas ao usar **Aviso** para o argumento **Opções** da ação **SairdoAccess**.

Você pode usar a ação **SalvarObjeto** de uma macro para salvar um objeto especificado sem precisar encerrar o Access ou fechar o objeto.

Para executar a ação **SairdoAccess** em um módulo do VBA (Visual Basic for Applications), use o método **Sair** do objeto **DoCmd**.

