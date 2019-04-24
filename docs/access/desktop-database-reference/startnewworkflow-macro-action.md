---
title: Ação da macro IniciarNovoFluxoDeTrabalho
TOCTitle: StartNewWorkflow macro action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1e37d72754531fc4dd51427eefb355a057d08073
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306395"
---
# <a name="startnewworkflow-macro-action"></a>Ação da macro IniciarNovoFluxoDeTrabalho


**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **IniciarNovoFluxoDeTrabalho** para iniciar um novo fluxo de trabalho para um item em uma lista vinculada do Microsoft SharePoint Foundation.

## <a name="setting"></a>Configuração

A ação **IniciarNovoFluxoDeTrabalho** tem o argumento a seguir.

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
<td><p><strong>Número de registro</strong></p></td>
<td><p>A posição do item na lista do SharePoint Foundation, começando com <strong>1</strong> para o primeiro item da lista, <strong>2</strong> para o segundo item e assim por diante. Você também pode inserir uma expressão para esse argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

  - A ação **IniciarNovoFluxoDeTrabalho** abre a caixa de diálogo **Iniciar Novo Fluxo de Trabalho**. Essa caixa de diálogo exibe todos os fluxos de trabalho disponíveis para o item especificado. Um fluxo de trabalho deve ser definido para a lista do SharePoint Foundation para que você possa iniciá-lo usando esta ação.

  - A ação **IniciarNovoFluxoDeTrabalho** pode ser usada somente depois de uma lista vinculada do SharePoint ter sido aberta e selecionada. Para abrir e selecionar a lista vinculada, use a ação **AbrirTabela**. Se a lista já estiver aberta, use a ação **SelecionarObjeto** para selecioná-la.

  - A ação **IniciarNovoFluxoDeTrabalho** tem o mesmo efeito de clicar com o botão direito do mouse em qualquer célula de uma lista vinculada do SharePoint enquanto ela está aberta no modo Folha de Dados, apontar para **Fluxo de Trabalho** e clicar em **Iniciar Novo Fluxo de Trabalho**.

  - Para executar a ação **IniciarNovoFluxoDeTrabalho** em um módulo do VBA, use o método **StartNewWorkflow** do objeto **DoCmd**.

