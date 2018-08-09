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
ms.openlocfilehash: a88da9e4973f819b398b5bdeda434ede14640797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772244"
---
# <a name="lockcustprop-cell-protection-section"></a>Célula LockCustProp (Seção Protection)

Estabelece se o usuário pode adicionar, excluir ou modificar dados da forma na interface do usuário (UI) usando a caixa de diálogo **Definir Dados da Forma** ou o menu de atalho para a janela **Dados da Forma**. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |
          O comando **Definir Dados da Forma** no menu de atalho da janela **Dados da Forma** é desabilitado.
  <br/> |
|FALSO  <br/> |
          O comando **Definir Dados da Forma** no menu de atalho da janela **Dados da Forma** é habilitado (padrão).
  <br/> |
   
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
|Índice da linha:  <br/> |**visRowLock** <br/> |
|Índice da célula:  <br/> |**visLockCustProp** <br/> |
   

