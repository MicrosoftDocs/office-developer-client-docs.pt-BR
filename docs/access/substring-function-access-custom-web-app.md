---
title: Função SubString (aplicativo da Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Retorna parte de uma expressão de texto.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433469"
---
# <a name="substring-function-access-custom-web-app"></a>Função SubString (aplicativo Web personalizado do Access)

Retorna parte de uma expressão de texto.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 **SubString** (*TextExpression*, *Start*, *Length*) 
  
A função **SubString** contém os argumentos a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *TextExpression*  <br/> |Uma expressão de texto.  <br/> |
| *Start*  <br/> |Uma expressão de números inteiros que especifica o local no qual começam os caracteres retornados. Se essa expressão for menor que 1, a expressão retornada começará no primeiro caractere que é especificado na expressão. Nesse caso, o número de caracteres que são retornados é o maior valor da soma de início + o comprimento -1 ou 0. Se o início for maior que o número de caracteres na expressão de valor, uma expressão de comprimento zero será retornada.  <br/> |
| *Length*  <br/> |Uma expressão com um número inteiro positivo, que especifica quantos caracteres da expressão serão retornados. Se for negativo, é gerado um erro e a política é encerrada. Se a soma do início e a duração forem maiores que o número de caracteres na expressão, o início da expressão de valor inserida no início é retornado.  <br/> |
   

