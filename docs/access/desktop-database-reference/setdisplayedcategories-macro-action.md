---
title: Ação da macro DefinirCategoriasExibidas
TOCTitle: SetDisplayedCategories macro action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f08b9a8980fc6f08a9f91366d38f65e4365a037e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314621"
---
# <a name="setdisplayedcategories-macro-action"></a>Ação da macro DefinirCategoriasExibidas


**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **DefinirCategoriasExibidas** para especificar quais categorias serão exibidas em **Navegar para Categoria** na barra de título do Painel de Navegação. Por exemplo, para que os usuários não possam mudar o Painel de Navegação para exibir objetos classificados por **Data da Criação**, use essa ação para ocultar essa opção na lista suspensa da barra de título.

## <a name="setting"></a>Setting

A ação **DefinirCategoriasExibidas** tem os seguintes argumentos.

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
<td><p><strong>Show</strong></p></td>
<td><p>Selecione <strong>Sim</strong> para mostrar a(s) categoria(s). Selecione <strong>Não</strong> para ocultá-la(s).</p></td>
</tr>
<tr class="even">
<td><p><strong>Categoria</strong></p></td>
<td><p>Digite ou selecione o nome da categoria que você deseja mostrar ou ocultar. Deixe em branco para mostrar ou ocultar todas as categorias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

  - A legenda da barra de título do Painel de Navegação indica o filtro que está atualmente ativo, caso haja algum filtro. Clique em qualquer lugar da barra para exibir a lista suspensa. Os itens que essa macro controla estão listados em **Navegar para Categoria**.

  - Essa ação apenas habilita ou desabilita a exibição das categorias especificadas; ela não executa a alternância de exibição do Painel de Navegação. Por exemplo, se você estiver exibindo objetos classificados por **Data de Criação** e usar a ação **DefinirCategoriasExibidas** para desabilitar a opção **Data de Criação**, o Access não alternará a categoria no Painel de Navegação.

  - Para executar a ação **DefinirCategoriasExibidas** em um módulo do VBA, use o método **SetDisplayedCategories** do objeto **DoCmd**.

