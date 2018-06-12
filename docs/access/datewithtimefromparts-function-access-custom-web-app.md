---
title: Função DateWithTimeFromParts (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Retorna uma data e hora com base em um ano especificado, mês, dia e hora.
ms.openlocfilehash: 8cc1fbe700d18c04d944793bcea889424b0cff3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765030"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>Função DateWithTimeFromParts (aplicativo da web personalizado do Access)

Retorna uma data e hora com base em um ano especificado, mês, dia e hora.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**DateWithTimeFromParts** (*Ano*, *mês*, *dia*, *hora*, *minuto*, *segundo*) 
  
A função **DateWithTimeFromParts** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Ano*  <br/> |Expressão de inteiro especificando um ano.  <br/> |
| *Month*  <br/> |Expressão de inteiro especificando um mês.  <br/> |
| *Dia*  <br/> |Expressão de inteiro especificando um dia.  <br/> |
| *Hora*  <br/> |Expressão de inteiro especificando horas.  <br/> |
| *Minuto*  <br/> |Expressão de inteiro especificando minutos.  <br/> |
| *Segundo*  <br/> |Expressão de inteiro especificando segundos.  <br/> |
   
## <a name="remarks"></a>Coment�rios

**DateWithTimeFromParts** retorna um valor de data/hora totalmente inicializado. Se os argumentos não são válidos, um erro será gerado. Se for necessário argumentos forem nulos, Null será retornado. 
  

