---
title: Função de atualização (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Retorna se uma operação de inserção ou atualização foi tentada no campo especificado.
ms.openlocfilehash: 1685d9f44bd167571b949a34d6c7b6993e63fbc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765259"
---
# <a name="update-function-access-custom-web-app"></a>Função de atualização (aplicativo da web personalizado do Access)

Retorna se uma operação de inserção ou atualização foi tentada no campo especificado.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Atualização** (*Coluna*) 
  
A função de **atualização** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Column*  <br/> |O nome do campo para verificar se há uma operação de inserção ou atualização.  <br/> |
   
## <a name="remarks"></a>Comentários

A função de **atualização** retorna TRUE, independentemente se uma tentativa INSERT ou UPDATE for bem-sucedido. 
  

