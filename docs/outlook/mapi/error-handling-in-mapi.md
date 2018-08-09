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
ms.openlocfilehash: 6f0ebd2112b65140a106a1376896f6de9c00da1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766505"
---
# <a name="error-handling-in-mapi"></a>Tratamento de erros no MAPI

**Aplica-se a**: Outlook 
  
Os valores de sucesso, aviso e erro são retornados usando um número de 32 bits, conhecido como resultado alça ou HRESULT. Um HRESULT não é realmente uma alça nada; ele é meramente um valor de 32 bits com vários campos codificados em que o valor. Um resultado de zero indica êxito e um resultado diferente de zero indica uma falha.
  
MAPI em plataformas de 32 bits funciona somente com valores HRESULT.
  
A ilustração a seguir mostra o formato HRESULT para plataformas de 32 bits.
  
**HRESULT format**
  
![Formato HRESULT] (media/amapi_49.gif "Formato HRESULT")
  
O bit de ordem alta no HRESULT indica se o valor de retorno representa sucesso ou falha. Se definido como zero, o valor indica sucesso. Se definida como 1, indica falha.
  
O R, C, N e bits r reservados no HRESULT.
  
O campo de recurso nas duas versões indica a área de responsabilidade para o erro. Há várias instalações, mas a maioria dos erros MAPI usar FACILITY_ITF para representar os erros de interface. Os recursos mais comuns que são usados atualmente são: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC e FACILITY_STORAGE. Se novas instalações forem necessárias, Microsoft aloca-las porque eles precisam ser exclusivas. A tabela a seguir descreve os vários campos de recurso.
  
|Instalações|Descrição|
|:-----|:-----|
|FACILITY_NULL  <br/> |Para obter códigos de status comuns amplamente aplicáveis como S_OK ou E_OUTOF_MEMORY; o valor for zero.  <br/> |
|FACILITY_ITF  <br/> |Para a maioria dos códigos de status retornados de métodos de interface; o valor é definido pela interface. Ou seja, os dois valores HRESULT com exatamente o mesmo valor 32-bit retornado de duas interfaces diferentes podem ter significados diferentes.  <br/> |
|FACILITY_DISPATCH  <br/> |Erros da interface para associação tardia [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) .  <br/> |
|FACILITY_RPC  <br/> |Para obter códigos de status retornados de chamadas de procedimento remoto.  <br/> |
|FACILITY_STORAGE  <br/> |Para obter códigos de status retornados de chamadas de método [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) ou [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) relativos ao armazenamento estruturado. Códigos de status com valores de código (16 bits inferiores) nos códigos de erro de intervalo do Windows (ou seja, menos de 256) têm o mesmo significado como os erros do Windows correspondentes.  <br/> |
   
O campo código é um número exclusivo atribuído para representar o erro ou aviso.
  

