[![MseeP.ai Security Assessment Badge](https://mseep.net/pr/wjessup-github-mcp-server-review-tools-badge.png)](https://mseep.ai/app/wjessup-github-mcp-server-review-tools)



Tools:

```
tools: [
      {
        name: "get_pull_request_review",
        description: "Get a specific pull request review",
        inputSchema: zodToJsonSchema(pullRequestReviews.GetPullRequestReviewSchema)
      },
      {
        name: "get_pull_request_comment",
        description: "Get a specific pull request review comment",
        inputSchema: zodToJsonSchema(pullRequestComments.GetPullRequestCommentSchema)
      },
      {
        name: "reply_to_pull_request_comment",
        description: "Add a reply to a specific pull request review comment",
        inputSchema: zodToJsonSchema(pullRequestComments.ReplyToPullRequestCommentSchema)
      },
      {
        name: "resolve_pull_request_review_thread",
        description: "Mark a pull request review thread as resolved",
        inputSchema: zodToJsonSchema(pullRequestReviews.ResolvePullRequestReviewThreadSchema)
      },
      {
        name: "check_pull_request_review_resolution",
        description: "Check if all threads in a pull request review are resolved",
        inputSchema: zodToJsonSchema(pullRequestReviews.CheckPullRequestReviewResolutionSchema)
      },
      {
        name: "get_pull_request_review_threads",
        description: "Get the threads in a specific pull request review",
        inputSchema: zodToJsonSchema(pullRequestReviews.GetPullRequestReviewThreadsSchema)
      },
      {
        name: "get_pull_request_threads",
        description: "Get all review threads for a pull request in a single call",
        inputSchema: zodToJsonSchema(pullRequestReviews.GetPullRequestThreadsSchema)
      },
      {
        name: "get_pull_request_thread",
        description: "Get a single pull request review thread with complete comment details",
        inputSchema: zodToJsonSchema(pullRequestReviews.GetPullRequestThreadSchema)
      }
    ],
```

install manually:

```
Yarn && Yarn start
```

Install into cursor:

```
{
  "mcpServers": {
    "github-pr-review-tools": {
      "command": "node",
      "args": ["~/Code/github-server-only/dist/index.js"], #put your repo location
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": <your code here>
      }
    }
  }
}
```


## Build

Docker build: (haven't tested)

```bash
docker build -t mcp/github -f src/github/Dockerfile .
```

## License

MIT License. This means you are free to use, modify, and distribute the software, subject to the terms and conditions of the MIT License. For more details, please see the LICENSE file in the project repository.

