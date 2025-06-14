this is my implementation of ddpm as described in https://arxiv.org/abs/2006.11239

few notes:
1. the generated samples aren't of the best quality but i think its mostly just b/c i stopped training early so it wouldn't take forever
   as u can see, loss decreased from 0.1057 to 0.0394 in 10 epochs
2. some things i could have incorporated is: cosine-beta schedule (instead of linear) as it prevents a large fraction of the 1000 steps just being a ton of noise with no inherent meaning,
   including the bottleneck part of the u-net, i excluded it so the model wouldn't be as big and would take less time for training
   based on how training progresses, could add learning rate scheduler if loss plateaus
