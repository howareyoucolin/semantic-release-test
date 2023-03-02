module.exports = {
    branches: [
        'main',
        'master',
        'next',
        { name: 'alpha', prerelease: true },
        { name: 'beta', prerelease: true },
        { name: 'hotfix', prerelease: true },
        { name: 'rc', prerelease: true },
    ],
    plugins: [
        [
            '@semantic-release/commit-analyzer',
            {
                preset: 'conventionalcommits',
                releaseRules: [
                    { type: 'build', scope: 'deps', release: 'patch' },
                    { type: 'style', release: 'minor' },
                ],
            },
        ],
        '@semantic-release/release-notes-generator',
        '@semantic-release/npm',
        '@semantic-release/github',
        [
            '@semantic-release/git',
            {
                message: 'chore(release): ${nextRelease.version}',
            },
        ],
    ],
}