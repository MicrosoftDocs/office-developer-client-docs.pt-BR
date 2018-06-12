---
title: Documentação do valor de retorno de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: f2b8f87987f93ec152d4986131a6b7990273c28d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767941"
---
# <a name="mapi-return-value-documentation"></a>Documentação do valor de retorno de MAPI

  
  
**Aplica-se a**: Outlook 
  
As entradas de referência nesta referência apenas os valores de retorno que requerem alguns tratamento pelos aplicativos cliente do documento. Os valores de retorno que indicam condições de erro comuns e podem ser deduzidos verificando da falha não são incluídos na documentação. Por exemplo, muitos métodos de interface podem retornar MAPI_E_INVALID_PARAMETER se um chamador Especifica o valor errado para um parâmetro de entrada. Esse valor geralmente não está listado no conjunto de valores de retorno esperados porque não há nenhuma necessidade para procurar especificamente MAPI_E_INVALID_PARAMETER e nenhuma necessidade de processá-la de forma diferente de qualquer outro tipo de erro. Por outro lado, alguns provedores de serviços não oferecem suporte a notificação de evento e retornarão MAPI_E_NO_SUPPORT ao método **Advise** feito por clientes através do **IMAPISession**. Como os clientes precisam explicitamente Verifique esse valor e forneça o código para manipular a condição que ele representa deve ele ocorrer, MAPI_E_NO_SUPPORT está incluído na lista de valores de retorno para [IMAPISession::Advise](imapisession-advise.md).
  
A tabela a seguir descreve os valores de erro que geralmente são retornados de métodos e as funções e exigem tratamento explícito por parte de um provedor de cliente ou serviço. Esses valores se encaixam em quatro categorias: valores que indicam a entrada de dados inválido, os valores que indicam problemas de recursos, os valores que indicam a incompatibilidade de conjunto de caracteres e valores que indicam a falha de uma origem desconhecida.
  
|**Valor retornado**|**Descrição**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Um ou mais dos parâmetros passado para o método ou funções não eram válidas.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Um ou mais valores para um parâmetro de sinalizadores não eram válidos.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Houve um problema ao gravar ou ler o disco.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |Espaço insuficiente em disco estava disponível para concluir a operação.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |Não há memória suficiente estava disponível para concluir a operação.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |Recursos do sistema insuficientes estavam disponíveis para concluir a operação.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |Existe uma incompatibilidade os conjuntos de caracteres compatíveis com o chamador e a implementação.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Ocorreu um erro de origem inesperado ou desconhecido.  <br/> |
   
As constantes que representam os valores de retorno de MAPI são listadas no MAPICODE. Arquivo de cabeçalho H. Algumas das constantes mapeiam para erros de Win32; o mapeamento das seguintes constantes para valores numéricos pode ser encontrado no arquivo de cabeçalho do Win32, WINERROR. H.
  
Erros relacionadas a dados inválidos passados por um chamador podem ser determinados por meio de um das funções de API de validação de parâmetro fornecidas pelo MAPI ou um conjunto de macros. 
  
Incompatibilidade de conjunto de caracteres surge quando qualquer uma das seguintes situações ocorrer:
  
- Um provedor de cliente ou serviço define o sinalizador MAPI_UNICODE em uma chamada de função ou o método e a implementação não dá suporte a Unicode. A definição MAPI_UNICODE indica que as sequências de caracteres passadas como entrada são cadeias de caracteres Unicode e que as sequências de caracteres passadas de volta como saída esperadas cadeias de caracteres Unicode.
    
- Um provedor de cliente ou serviço não defina o sinalizador MAPI_UNICODE em uma chamada de função ou o método e a implementação só oferece suporte a Unicode.
    

