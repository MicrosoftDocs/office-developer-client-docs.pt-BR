---
title: Códigos de erro do provedor do Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: Os provedores devem retornar os erros ao chamador usando um dos códigos de erro exibidos na tabela a seguir.
ms.openlocfilehash: 22a6e8d4ebf87157eaee630cc47f9f363150e839
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359854"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Códigos de erro do provedor do Outlook Social Connector

Os provedores devem retornar os erros ao chamador usando um dos códigos de erro exibidos na tabela a seguir. 
  
|**Erro**|**Código do erro (hexadecimal)**|**Descrição**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |Falha de autenticação na rede do site de rede social.  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |Nenhuma conexão está disponível para conectar ao site de rede social.  <br/> |
|OSC_E_FAIL  <br/> |0x80004005  <br/> |Erro de falha geral.  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |Um erro interno ocorreu devido a uma operação inválida.  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0x80070057  <br/> |Um argumento inválido foi transmitido a uma função.  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |Nenhuma alteração ocorreu desde a última sincronização.   <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |Um recurso não pode ser encontrado.  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |A solicitação ao site de rede social é válida mas não foi implementada pelo site de rede social.  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |Ocorreu um erro de memória insuficiente.  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |O provedor de OSC negou permissão ao recurso.  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |A versão do servidor para configurar a conta da rede social não é suportada.   <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |O provedor não oferece suporte para esta versão de extensibilidade do provedor de OSC.  <br/> |
   
## <a name="remarks"></a>Comentários

Valores de sucesso, aviso e erro são retornados usando um número de 32 bits que se chama identificador de resultado ou **HRESULT**. Um **HRESULT** não é um identificador de coisa alguma; ele é simplesmente um valor de 32 bits com vários campos codificados no valor.  Um resultado positivo indica sucesso com status, um resultado zero indica sucesso sem status (S_OK) e um resultado negativo indica falhar.  
  

