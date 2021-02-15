---
title: Ação da macro AbrirMódulodoVisualBasic
TOCTitle: OpenVisualBasicModule macro action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 55af2ce884b26b4c3df219e7d1986e7dc2e4c8ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288277"
---
# <a name="openvisualbasicmodule-macro-action"></a>Ação da macro AbrirMódulodoVisualBasic

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **AbrirMódulodoVisualBasic** para abrir um módulo do VBA (Visual Basic for Applications) especificado em um procedimento especificado. Este pode ser um procedimento Sub, um procedimento Function ou um procedimento de evento.

> [!NOTE]
> Essa ação não será permitida se o banco de dados não for confiável. 

## <a name="setting"></a>Setting

A ação **AbrirMódulodoVisualBasic** tem os seguintes argumentos.

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
<td><p><strong>Nome do Módulo</strong></p></td>
<td><p>O nome do módulo que será aberto. Você pode deixar este argumento em branco para pesquisar em todos os módulos padrão do banco dedados se há um procedimento e abrir o módulo apropriado nesse procedimento. Se você executar uma macro que contém a ação <strong>AbrirMódulodoVisualBasic</strong> em um banco de dados biblioteca, o Microsoft Access procurará o módulo com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Procedimento</strong></p></td>
<td><p>O nome do procedimento para o qual você deseja abrir o módulo. Se você deixar este argumento em branco, o módulo será aberto na seção Declarações.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Você precisa digitar um nome válido no argumento **Nome do Módulo** ou **Nome do Procedimento**.


## <a name="remarks"></a>Comentários

Você pode usar esta ação para abrir um procedimento de evento especificando o argumento **Nome do Módulo** e o argumento **Nome do Procedimento**. For example, to open the **Click** event procedure of the PrintInvoice button on the form Orders, set the **Module Name** argument to **Form.Orders** and set the **Procedure Name** argument to **PrintInvoice \_ Click**. Para exibir o procedimento de evento de um formulário ou relatório, este precisa estar aberto.

Da mesma maneira, para abrir um procedimento em um módulo de classe, especifique o nome do módulo, embora não seja necessário abrir o módulo de classe.

Para abrir um procedimento particular, o módulo que o contém precisa estar aberto.

Esta ação equivale a clicar com o botão direito do mouse em um módulo do Painel de Navegação e clicar em **Modo Design**. Ela também permite especificar um nome de procedimento e pesquisar nos módulos padrão de um banco de dados se há procedimentos.

> [!TIP]
> [!DICA] Você pode selecionar um módulo do Painel de Navegação e arrastá-lo para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirMódulodoVisualBasic** que abre o módulo na seção Declarações.

Para executar a ação **AbrirMódulodoVisualBasic** em um módulo do VBA, use o método **AbrirMódulo** do objeto **DoCmd**.

