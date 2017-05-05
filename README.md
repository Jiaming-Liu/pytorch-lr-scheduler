# pytorch-lr-scheduler
Bring some LR schedulers from [Keras](https://keras.io/) to [PyTorch](http://pytorch.org/). This repo currently includes ReduceLROnPlateau.

See also: https://github.com/Jiaming-Liu/pytorch/tree/LR-Scheduler

Demo of ReduceLROnPlateau: 

    optimizer = torch.optim.SGD(model.parameters(), lr=0.1, momentum=0.9)
	scheduler = ReduceLROnPlateau(optimizer, 'min') # set up scheduler
	for epoch in range(10):
	    train(...)
	    val_acc, val_loss = validate(...)
	    scheduler.step(val_loss, epoch) # update lr if needed
