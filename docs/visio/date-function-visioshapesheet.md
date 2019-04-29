---
title: Função DATE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Retorna a data representada por ano, mês e dia formatados de acordo com o estilo de data abreviada das Configurações Regionais do sistema. Os valores de ano, mês e dia refletem o calendário gregoriano.
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360330"
---
# <a name="date-function-visioshapesheet"></a>Função DATE (VisioShapeSheet)

Retorna a data representada por *ano, mês* e *dia* formatados de acordo com o estilo de data abreviada das Configurações Regionais do sistema. Os valores de *ano*, *mês* e *dia*  refletem o calendário gregoriano. 
  
## <a name="syntax"></a>Sintaxe

DATE(** *ano* **, ** *mês* **, ** *dia* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _ano_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O ano.  <br/> |
| _mês_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O mês.  <br/> |
| _dia_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O dia.  <br/> |
   
## <a name="example-1"></a>Exemplo 1

DATE(1999,6,7)
  
Retornará o valor que representa 07/06/1999.
  
## <a name="example-2"></a>Exemplo 2

DATE(1999,6,7) + 4 ed.
  
Retornará o valor que representa 11/06/99.
  
## <a name="example-3"></a>Exemplo 3

FORMAT(DATE(1999,10,14),"C")
  
Retornará o valor que representa terça-feira, 14 de outubro de 1999.
  

