---
title: Função DateFromParts (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Retorna um valor de data para o ano, mês e dia especificados.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423220"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Função DateFromParts (aplicativo Web personalizado do Access)

Retorna um valor de data para o ano, mês e dia especificados.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**DateFromParts** (*Ano*, *mês*, *dia*) 
  
A função **DateFromParts** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Year*  <br/> |Expressão de inteiro que especifica um ano.  <br/> |
| *Month*  <br/> |Expressão de inteiro que especifica um mês, de 1 a 12.  <br/> |
| *Day*  <br/> |Expressão de inteiro que especifica um dia.  <br/> |
   
## <a name="remarks"></a>Comentários

**DateFromParts** retorna um valor de data com a parte de data definida para o ano, mês e dia especificados, e a parte de hora definida como padrão. Se os argumentos não forem válidos, ocorrerá um erro. Se os argumentos necessários forem nulos, NULL será retornado. 
  
## <a name="example"></a>Exemplo

A expressão a seguir usa a função **DateFromParts** para calcular o primeiro dia do mês atual. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



