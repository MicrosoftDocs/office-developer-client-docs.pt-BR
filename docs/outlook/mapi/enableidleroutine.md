---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 00b5c123e588636654fb4287cc7b45500d47d89c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766493"
---
# <a name="enableidleroutine"></a>EnableIdleRoutine

  
  
**Aplica-se a**: Outlook 
  
Habilita ou desabilita uma rotina de ociosidade [FNIDLE](fnidle.md) com base. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a>Par�metros

 _ftg_
  
> [in] Marca de função que identifica a rotina ociosa para ser habilitada ou desabilitada. 
    
 _fEnable_
  
> [in] Contém TRUE se o mecanismo de ociosidade deve habilitar a rotina ociosa ou FALSE se ele deve desabilitá-lo.
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) : 
  
|**Função de rotina ociosa**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Altera as características de uma rotina de ociosidade registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina de ociosidade registrada do sistema MAPI.  <br/> |
|**EnableIdleRoutine** <br/> |Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** tomar como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**. 
  
Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar. Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade. 
  

