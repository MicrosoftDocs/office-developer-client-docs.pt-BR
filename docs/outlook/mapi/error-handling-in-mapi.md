---
title: Tratamento de erros no MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287274"
---
# <a name="error-handling-in-mapi"></a>Tratamento de erros no MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os valores Success, Warning e Error são retornados usando um número de 32 bits conhecido como um identificador de resultado ou HRESULT. No entanto, o HRESULT não é um manipulador para nada; é meramente um valor de 32 bits com vários campos codificados no valor. Um resultado zero indica êxito e um resultado diferente de zero indica falha.
  
MAPI em plataformas de 32 bits funciona unicamente com valores HRESULT.
  
A ilustração a seguir mostra o formato HRESULT para plataformas de 32 bits.
  
**HRESULT format**
  
![Formato HRESULT] (media/amapi_49.gif "Formato HRESULT")
  
O bit de ordem superior no HRESULT indica se o valor de retorno representa êxito ou falha. Se definido como zero, o valor indica êxito. Se definido como 1, indica falha.
  
Os bits R, C, N e R são reservados no HRESULT.
  
O campo recurso em ambas as versões indica a área de responsabilidade do erro. Há vários recursos, mas a maior parte dos erros MAPI usa o FACILITY_ITF para representar erros de interface. Os recursos mais comuns usados atualmente são: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC e FACILITY_STORAGE. Se novos recursos forem necessários, a Microsoft os alocará porque eles precisam ser exclusivos. A tabela a seguir descreve os vários campos de recurso.
  
|Facility|Descrição|
|:-----|:-----|
|FACILITY_NULL  <br/> |Para códigos de status comuns amplamente aplicáveis, como S_OK ou E_OUTOF_MEMORY; o valor é zero.  <br/> |
|FACILITY_ITF  <br/> |Para a maioria dos códigos de status retornados dos métodos de interface; o valor é definido pela interface. Ou seja, dois valores HRESULT com exatamente o mesmo valor de 32 bits retornado de duas interfaces diferentes podem ter significados diferentes.  <br/> |
|FACILITY_DISPATCH  <br/> |Para erros de [](https://msdn.microsoft.com/library/ms221608.aspx) interface de associação tardia.  <br/> |
|FACILITY_RPC  <br/> |Para códigos de status retornados de chamadas de procedimento remoto.  <br/> |
|FACILITY_STORAGE  <br/> |Para códigos de status retornados das chamadas de método [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) ou [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) relacionadas ao armazenamento estruturado. Os códigos de status com valores de código (menores de 16 bits) no intervalo de códigos de erro do Windows (ou seja, menos de 256) têm o mesmo significado dos erros do Windows correspondentes.  <br/> |
   
O campo de código é um número exclusivo que é atribuído para representar o erro ou aviso.
  

