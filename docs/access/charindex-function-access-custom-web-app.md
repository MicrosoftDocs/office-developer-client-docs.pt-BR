---
title: Função CharIndex (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Pesquisas uma expressão de texto para outra expressão de texto e retorna suas Iniciando posição se encontrado.
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765083"
---
# <a name="charindex-function-access-custom-web-app"></a>Função CharIndex (aplicativo da web personalizado do Access)

Pesquisas uma expressão de texto para outra expressão de texto e retorna suas Iniciando posição se encontrado.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

**CharIndex** (*TextExpression*, *WithinText*, [*Iniciar*]) 
  
|**Nome do Argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Sim  <br/> |Uma expressão de texto que contém o texto a ser localizado.  <br/> |
| *WithinText*  <br/> |Sim  <br/> |A expressão de texto a ser pesquisado.  <br/> |
| *Start*  <br/> |Não  <br/> |Um inteiro que especifica o local em *WithinText* para iniciar a pesquisa. Se *Iniciar* não for especificado, for um número negativo ou for 0, a pesquisa começa no início do *WithinText* .  <br/> |
   
## <a name="remarks"></a>Comentários

Se *TextExpression* ou *WithinText* for NULL, *CharIndex* retornará NULL. 
  
Se *TextExpression* não for encontrado na *WithinText*, *CharIndex* retornará 0. 
  
A posição inicial retornada é baseado em 1, não baseado em 0.
  

