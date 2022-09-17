# java-reactive-programming-course

This repository contains the code samples, assignments etc .

Mono :: It emits 0 or 1 items , followed by an onComplete /onError.
Type -> Condition -> What to use

Create Mono -> Data already present -> Mono.just(data)
Create Mono -> Data to be calculated -> Mono.fromSupplier(()-> getData()) ; Mono.fromCallable(()->getData()).
Create Mono -> Data is coming from async completableFuture -> Mono.fromFuture(future)
Create Mono -> Emit empty once a given runnable is complete -> Mono.fromRunnable(runnable).
Pass Mono as argument -> Function accepts a Mono<Address> but i donot have data -> Mono.empty().
Return Mono -> Function needs to return a Mono -> Mono.error() ; Mono.empty ; above creation types

