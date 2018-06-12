---
title: Função TimeFromParts (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Retorna um valor de tempo com base em partes especificadas.
ms.openlocfilehash: 55a4d1c31fdd2248e3e154d83e803d9f5a5ebb06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765235"
---
# <a name="timefromparts-function-access-custom-web-app"></a>Função TimeFromParts (aplicativo da web personalizado do Access)

Retorna um valor de tempo com base em partes especificadas.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **TimeFromParts** (*Hora*, *minuto*, *segundo*) 
  
A função **TimeFromParts** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Hora*  <br/> |Expressão de inteiro especificando horas.  <br/> |
| *Minuto*  <br/> |Expressão de inteiro especificando minutos.  <br/> |
| *Segundo*  <br/> |Expressão de inteiro especificando segundos.  <br/> |
   
## <a name="see-also"></a>Confira também

 **TimeFromParts** retorna um valor de tempo totalmente inicializado. Se os argumentos são inválidos, um erro é gerado. Se qualquer um dos parâmetros forem nulo, nulo será retornado. 
  

