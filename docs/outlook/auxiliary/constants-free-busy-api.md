---
title: Constantes (API do serviço de disponibilidade)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Este tópico contém definições constantes, identificadores de classe e identificadores de interface para a API de Livre/Ocupado.
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431530"
---
# <a name="constants-freebusy-api"></a>Constantes (API do serviço de disponibilidade)

Este tópico contém definições constantes, identificadores de classe e identificadores de interface para a API de Livre/Ocupado.
  
## <a name="constants"></a>Constantes

|**Constante**|**Definição**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Conforme definido no arquivo de título winerror.h do Microsoft Software Development Kit do Windows (SDK do Windows).*  <br/> |
|E_OUTOFMEMORY  <br/> | *Conforme definido no arquivo de título winerror.h do SDK do Windows.*  <br/> |
|S_FALSE  <br/> | *Conforme definido no arquivo de título winerror.h do SDK do Windows.*  <br/> |
|S_OK  <br/> | *Conforme definido no arquivo de título winerror.h do SDK do Windows.*  <br/> |
   
## <a name="interface-identifiers"></a>Identificadores de interface

Para os identificadores de interface a seguir, suponha que DEFINE_GUID macro definida no arquivo de título do SDK do Windows guiddef.h para associar o nome simbólico guid ao seu valor.
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  

