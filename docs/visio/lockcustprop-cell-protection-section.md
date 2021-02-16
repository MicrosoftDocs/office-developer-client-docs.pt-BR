---
title: Célula LockCustProp (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Estabelece se o usuário pode adicionar, excluir ou modificar dados da forma na interface do usuário (UI) usando a caixa de diálogo Definir Dados da Forma ou o menu de atalho para a janela Dados da Forma.
ms.openlocfilehash: 001123f3bd08d35f6f8e4874e20f2ee073835494
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422520"
---
# <a name="lockcustprop-cell-protection-section"></a>Célula LockCustProp (Seção Protection)

Estabelece se o usuário pode adicionar, excluir ou modificar dados da forma na interface do usuário (UI) usando a caixa de diálogo **Definir Dados da Forma** ou o menu de atalho para a janela **Dados da Forma**. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O comando **Definir Dados da Forma** no menu de atalho da janela **Dados da Forma** é desabilitado.  <br/> |
|FALSE  <br/> |O comando **Definir Dados da Forma** no menu de atalho da janela **Dados da Forma** é habilitado (padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Um valor VERDADEIRO não evita que um usuário altere o valor de um item de dados da forma ou altere a seção Shape Data na janela ShapeSheet. 
  
Para obter uma referência para a célula LockCustProp pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LockCustProp  <br/> |
   
Para obter uma referência para a célula LockCustProp pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowLock** <br/> |
|Índice de célula:  <br/> |**visLockCustProp** <br/> |
   

