---
title: Função Update (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Retorna se uma operação INSERT ou UPDATE foi tentada no campo especificado.
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410914"
---
# <a name="update-function-access-custom-web-app"></a>Função Update (aplicativo Web personalizado do Access)

Retorna se uma operação INSERT ou UPDATE foi tentada no campo especificado.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Update** (*Column*) 
  
A **função** Update contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Column*  <br/> |O nome do campo para verificar se há uma operação INSERT ou UPDATE.  <br/> |
   
## <a name="remarks"></a>Comentários

A **função Update** retorna VERDADEIRO independentemente de uma tentativa insert ou UPDATE ter êxito. 
  

