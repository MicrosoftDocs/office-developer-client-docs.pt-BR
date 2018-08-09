---
title: Constantes (API de livre/ocupado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Este tópico contém as definições de constantes, identificadores de classe e os identificadores de interface para a API de disponibilidade.
ms.openlocfilehash: ec909d449dc9075959fc9c047457577efd52ec3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765801"
---
# <a name="constants-freebusy-api"></a>Constantes (API de livre/ocupado)

Este tópico contém as definições de constantes, identificadores de classe e os identificadores de interface para a API de disponibilidade.
  
## <a name="constants"></a>Constantes

|**Constante**|**Definição**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Conforme definido em Winerror de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows.*  <br/> |
|E_OUTOFMEMORY  <br/> | *Conforme definido em Winerror de arquivo de cabeçalho do SDK do Windows.*  <br/> |
|S_FALSE  <br/> | *Conforme definido em Winerror de arquivo de cabeçalho do SDK do Windows.*  <br/> |
|S_OK  <br/> | *Conforme definido em Winerror de arquivo de cabeçalho do SDK do Windows.*  <br/> |
   
## <a name="interface-identifiers"></a>Identificadores de interface

Para os seguintes identificadores de interface, pressupõem que a macro DEFINE_GUID definida no guiddef.h de arquivo de cabeçalho do SDK do Windows para associar o nome simbólico do GUID a seu valor.
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  

