---
title: Função CharIndex (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Pesquisa uma expressão de texto em busca de outra expressão de texto e retorna sua posição inicial, se encontrada.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423129"
---
# <a name="charindex-function-access-custom-web-app"></a>Função CharIndex (aplicativo Web personalizado do Access)

Pesquisa uma expressão de texto em busca de outra expressão de texto e retorna sua posição inicial, se encontrada.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

**CharIndex** (*TextExpression*, *WithinText*, [*Start*]) 
  
|**Nome do Argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Sim  <br/> |Uma expressão de texto que contém o texto a ser localizado.  <br/> |
| *WithinText*  <br/> |Sim  <br/> |A expressão de texto a ser pesquisada.  <br/> |
| *Start*  <br/> |Não  <br/> |Um inteiro que especifica o local em  *WithinText*  para iniciar a pesquisa. Se  *Start*  não for especificado, for um número negativo ou for 0, a pesquisa começará no início de  *WithinText*  .  <br/> |
   
## <a name="remarks"></a>Comentários

Se  *TextExpression ou*  *WithinText*  for NULL,  *CharIndex*  retornará NULL. 
  
Se  *TextExpression*  não for encontrado dentro  *de WithinText*,  *CharIndex*  retornará 0. 
  
A posição inicial retornada é baseada em 1, não baseada em 0.
  

