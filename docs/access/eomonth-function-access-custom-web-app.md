---
title: Função FIMMÊS (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Retorna o último dia do mês antes ou o número de meses especificado.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437452"
---
# <a name="eomonth-function-access-custom-web-app"></a>Função FIMMÊS (aplicativo Web personalizado do Access)

Retorna o último dia do mês antes ou o número de meses especificado.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **FIMMÊS** (*Data*, *NumberOfMonth*) 
  
O **FIMMÊS** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Date*  <br/> |A data de início no formato de data/hora ou em uma representação de texto aceita de uma data.  <br/> |
| *NumberOfMonth*  <br/> |Um número que representa o número de meses antes ou depois da *Data* .  <br/> |
   
## <a name="remarks"></a>Comentários

Se *Data* não for uma data válida, **FIMMÊS** retornará um erro. 
  
Se *Date* mais *NumberOfMonth* gerar uma data inválida, **FIMMÊS** retornará um erro. 
  

