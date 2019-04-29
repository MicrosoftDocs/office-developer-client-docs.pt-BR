---
title: Função TimeFromParts (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Retorna um valor de tempo com base em partes especificadas.
ms.openlocfilehash: 8e2105140056bc65e9af0a6eda6e40fc44caed1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417991"
---
# <a name="timefromparts-function-access-custom-web-app"></a>Função TimeFromParts (aplicativo Web personalizado do Access)

Retorna um valor de tempo com base em partes especificadas.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **TimeFromParts** (*Hora*, *minuto*, *segundo*) 
  
A função **TimeFromParts** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Hour*  <br/> |Expressão de inteiro especificando horas.  <br/> |
| *Minute*  <br/> |Expressão de inteiro especificando minutos.  <br/> |
| *Second*  <br/> |Expressão de inteiro especificando segundos.  <br/> |
   
## <a name="see-also"></a>Confira também

 **TimeFromParts** retorna um valor de hora totalmente inicializado. Se os argumentos forem inválidos, um erro será gerado. Se qualquer um dos parâmetros for NULL, NULL será retornado. 
  

