---
title: Função Month (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Retorna um inteiro que representa o mês da data especificada.
ms.openlocfilehash: 5e4a583a5a299456e57b90d7cef41a32b0a6ffba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765205"
---
# <a name="month-function-access-custom-web-app"></a>Função Month (aplicativo da web personalizado do Access)

Retorna um inteiro que representa o mês da data especificada.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Mês** (*Data*) 
  
A função **Month** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Date*  <br/> |Uma expressão que pode ser resolvida como um valor de data/hora.  <br/> |
   
## <a name="remarks"></a>Comentários

 **Mês** retorna o mesmo valor que **DatePart** (mês, data). 
  
Se *Data* contiver apenas uma parte do tempo, o valor de retorno é 1, o mês de base. 
  

