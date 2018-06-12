---
title: Função FIMMÊS (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Retorna o último dia do mês antes ou do número especificado de meses.
ms.openlocfilehash: cee42c4e5cb3a24b2e702673238ac9ee09bc7372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765051"
---
# <a name="eomonth-function-access-custom-web-app"></a>Função FIMMÊS (aplicativo da web personalizado do Access)

Retorna o último dia do mês antes ou do número especificado de meses.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **FIMMÊS** (*Data*, *NumberOfMonth*) 
  
O **FIMMÊS** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Date*  <br/> |A data de início em formato de data/hora, ou em uma representação em texto aceitos de uma data.  <br/> |
| *NumberOfMonth*  <br/> |Um número que representa o número de meses antes ou depois da *Data* .  <br/> |
   
## <a name="remarks"></a>Coment�rios

Se *Data* não for uma data válida, **FIMMÊS** retornará um erro. 
  
Se a *Data* mais *NumberOfMonth* gerarem uma data inválida, **FIMMÊS** retornará um erro. 
  

