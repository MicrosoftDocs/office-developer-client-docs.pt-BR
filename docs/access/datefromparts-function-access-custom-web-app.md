---
title: Função DateFromParts (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Retorna um valor de data para o ano especificado, mês e dia.
ms.openlocfilehash: 5a2ff76d99076cf9f53b0dce8c5019f38d910f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765032"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Função DateFromParts (aplicativo da web personalizado do Access)

Retorna um valor de data para o ano especificado, mês e dia.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**DateFromParts** (*Ano*, *mês*, *dia*) 
  
A função **DateFromParts** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Ano*  <br/> |Expressão de inteiro especificando um ano.  <br/> |
| *Month*  <br/> |Expressão de inteiro especificando um mês, de 1 a 12.  <br/> |
| *Dia*  <br/> |Expressão de inteiro especificando um dia.  <br/> |
   
## <a name="remarks"></a>Coment�rios

**DateFromParts** retorna um valor de data com a parte da data definida como a parte de hora definido como o padrão e dia, mês e ano especificado. Se os argumentos não são válidos, um erro é gerado. Se for necessário argumentos são nulos, nulo será retornado. 
  
## <a name="example"></a>Example

A expressão a seguir utiliza a função **DateFromParts** para calcular o primeiro dia do mês atual. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



