---
title: Códigos de erro de provedor do Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: Provedores devem retornar erros ao chamador usando um dos códigos de erro mostrados na tabela a seguir.
ms.openlocfilehash: 9e9abfda5930926a873ac37d3372eff7100be8a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770949"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Códigos de erro de provedor do Outlook Social Connector

Provedores devem retornar erros ao chamador usando um dos códigos de erro mostrados na tabela a seguir. 
  
|**Erro**|**Código de erro (hexadecimal)**|**Descrição**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |Falha na autenticação na rede do site de rede social.  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |Nenhuma conexão está disponível para conectar ao site de rede social.  <br/> |
|OSC_E_FAIL  <br/> |0x80004005  <br/> |Erro de falha geral.  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |Ocorreu um erro interno devido a uma operação inválida.  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0x80070057  <br/> |Um argumento inválido foi passado para uma função.  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |Sem alterações ocorreram desde a última sincronização.  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |Um recurso não pode ser encontrado.  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |A solicitação para o site de rede social é válida, mas não foi implementada pelo site de rede social.  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |Ocorreu um erro de falta de memória.  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |O provedor do OSC negado permissão para o recurso.  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |Não há suporte para a versão do servidor para configurar a conta de redes sociais.  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |O provedor não oferece suporte para esta versão do estensibilidade do provedor do OSC.  <br/> |
   
## <a name="remarks"></a>Comentários

Êxito, aviso e valores de erro são retornados por meio de um número de 32 bits que é chamado de uma alça de resultado ou **HRESULT**. Um **HRESULT** não é um identificador para qualquer coisa; é meramente um valor de 32 bits que possui vários campos codificados no valor. Um resultado positivo indica sucesso com status, um resultado de zero indica êxito sem status (S_OK) e um resultado negativo indica uma falha. 
  

