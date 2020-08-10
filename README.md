# RecursivePipelineDemo
This repo contains a Recursive Azure DevOps Pipeline Demo. It is designed as a Proof of concept for how you could have both:
- A primary pipeline which you can trigger manually, or by Commit/PR.
- A parent pipeline which calls the Primary pipeline on a schedule with a source-controlled set of parameters.

This allows for redeployment of an environment on a schedule using a "last known good configuration", while still allowing the same pipeline to be used to deploy and test newly written code. 

Next steps I would consider for this would be to configure automatic tagging of the Builds. This would enable you to simply deploy the "latest" set of signed-off artifacts to the environment without having to change your scheduled pipeline.