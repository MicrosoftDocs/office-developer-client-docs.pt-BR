---
title: Função month (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Retorna um inteiro que representa o mês da data especificada.
ms.openlocfilehash: 0ca7059a2fd6dad1f9790ad6f4eafe7affa014dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308138"
---
# <a name="month-function-access-custom-web-app"></a>Função month (aplicativo Web personalizado do Access)

Retorna um inteiro que representa o mês da data especificada.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Mês** (*Data*) 
  
A função **month** contém o argumento a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Date*  <br/> |Uma expressão que pode ser resolvida como um valor de data/hora.  <br/> |
   
## <a name="remarks"></a>Comentários

 **Month** retorna o mesmo valor que **datepart** (mês, Data). 
  
Se *Date* contiver apenas uma parte de hora, o valor de retorno será 1, o mês base. 
  

